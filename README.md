# lane11-native

Researcher-owned fixture for lane-11: does GitHub's native `required_signatures`
ruleset rule evaluate a **newly pushed** commit that carries a valid signature
produced by the v0 fleet signing oracle?

`ankuhax10/test` cannot answer this: the forged commit `5c16462` is the parentless
ROOT of every branch there, so it is always "accessible from other branches" and
is excluded from ruleset evaluation. Here `main` is an unrelated researcher commit,
so a force-update of `demo/enforced` to `5c16462` makes it a genuinely new commit
for the rule to check.
