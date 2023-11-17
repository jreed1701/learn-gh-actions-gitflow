# learn-gh-actions-gitflow

Just a repo to teach myself gitflow using github actions.

Different Actions for:
- main:
  - When PR from develop to main branch happens main-branch-pr-actions.yml runs
  - After the PR and when main branch is pushed to - main-branch-after-merge-actions.yml runs
- develop:
  - When any feature branch updates the develop branch - develop-branch-actions.yml runs
- all other branches.
  - Any other branch other than main or develop, runs on every-other-branch-actions.yml.

When main branch is merged, the action computes the next tag and rolls the version and creates the release. Nothing
extra required of the user.  User could go back and add extra release artifacts if needed.
