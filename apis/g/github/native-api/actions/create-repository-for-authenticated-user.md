# Create Repository for Authenticated User with GitHub

Creates a repository for the authenticated GitHub user.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/repos`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Create Repository for Authenticated User](https://docs.github.com/en/rest/repos/repos#create-a-repository-for-the-authenticated-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the repository. |
| `description` | body | `string` | no | A short description of the repository. |
| `homepage` | body | `string` | no | A URL with more information about the repository. |
| `private` | body | `boolean` | no | Whether the repository is private. |
| `has_issues` | body | `boolean` | no | Whether issues are enabled. |
| `has_projects` | body | `boolean` | no | Whether projects are enabled. |
| `has_wiki` | body | `boolean` | no | Whether the wiki is enabled. |
| `has_discussions` | body | `boolean` | no | Whether discussions are enabled. |
| `team_id` | body | `number` | no | The ID of the team that will be granted access to this repository when applicable. |
| `auto_init` | body | `boolean` | no | Whether the repository is initialized with a minimal README. |
| `gitignore_template` | body | `string` | no | The desired language or platform to apply to the .gitignore. |
| `license_template` | body | `string` | no | The license keyword of the open source license for this repository. |
| `allow_squash_merge` | body | `boolean` | no | Whether to allow squash merges for pull requests. |
| `allow_merge_commit` | body | `boolean` | no | Whether to allow merge commits for pull requests. |
| `allow_rebase_merge` | body | `boolean` | no | Whether to allow rebase merges for pull requests. |
| `allow_auto_merge` | body | `boolean` | no | Whether to allow auto-merge to be used on pull requests. |
| `delete_branch_on_merge` | body | `boolean` | no | Whether to delete head branches when pull requests are merged. |
| `squash_merge_commit_title` | body | `list<string>` | no | The default value for a squash merge commit title. Accepted values: `0`, `1`. |
| `squash_merge_commit_message` | body | `list<string>` | no | The default value for a squash merge commit message. Accepted values: `0`, `1`, `2`. |
| `merge_commit_title` | body | `list<string>` | no | The default value for a merge commit title. Accepted values: `0`, `1`. |
| `merge_commit_message` | body | `list<string>` | no | The default value for a merge commit message. Accepted values: `0`, `1`, `2`. |
| `has_downloads` | body | `boolean` | no | Whether downloads are enabled. |
| `is_template` | body | `boolean` | no | Whether this repository acts as a template that can be used to generate new repositories. |
