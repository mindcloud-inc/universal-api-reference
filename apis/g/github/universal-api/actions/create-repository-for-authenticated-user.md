# GitHub: Create Repository for Authenticated User

Creates a repository for the authenticated GitHub user.

```
POST https://connect.mindcloud.co/v1/universal/github/latest/actions/create-repository-for-authenticated-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/github/latest/actions/create-repository-for-authenticated-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/github/latest/actions/create-repository-for-authenticated-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the repository. |
| `description` | string | no | A short description of the repository. |
| `private` | boolean | no | Whether the repository is private. |
| `auto_init` | boolean | no | Whether the repository is initialized with a minimal README. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `homepage` | string | no | A URL with more information about the repository. |
| `has_issues` | boolean | no | Whether issues are enabled. |
| `has_projects` | boolean | no | Whether projects are enabled. |
| `has_wiki` | boolean | no | Whether the wiki is enabled. |
| `has_discussions` | boolean | no | Whether discussions are enabled. |
| `team_id` | number | no | The ID of the team that will be granted access to this repository when applicable. |
| `gitignore_template` | string | no | The desired language or platform to apply to the .gitignore. |
| `license_template` | string | no | The license keyword of the open source license for this repository. |
| `allow_squash_merge` | boolean | no | Whether to allow squash merges for pull requests. |
| `allow_merge_commit` | boolean | no | Whether to allow merge commits for pull requests. |
| `allow_rebase_merge` | boolean | no | Whether to allow rebase merges for pull requests. |
| `allow_auto_merge` | boolean | no | Whether to allow auto-merge to be used on pull requests. |
| `delete_branch_on_merge` | boolean | no | Whether to delete head branches when pull requests are merged. |
| `squash_merge_commit_title` | list<string> | no | The default value for a squash merge commit title. One of: `0`, `1`. |
| `squash_merge_commit_message` | list<string> | no | The default value for a squash merge commit message. One of: `0`, `1`, `2`. |
| `merge_commit_title` | list<string> | no | The default value for a merge commit title. One of: `0`, `1`. |
| `merge_commit_message` | list<string> | no | The default value for a merge commit message. One of: `0`, `1`, `2`. |
| `has_downloads` | boolean | no | Whether downloads are enabled. |
| `is_template` | boolean | no | Whether this repository acts as a template that can be used to generate new repositories. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GitHub API returns.

## Native endpoint

Through the native GitHub API, this operation is `POST /user/repos` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-repository-for-authenticated-user.md) for the provider-specific parameters and requirements.

