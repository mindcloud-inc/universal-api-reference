# GitHub: Create Release

Creates a release in a GitHub repository.

```
POST https://connect.mindcloud.co/v1/universal/github/latest/actions/create-release
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/github/latest/actions/create-release" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "owner": "string",
  "repo": "string",
  "tag_name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/github/latest/actions/create-release', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "owner": "string",
    "repo": "string",
    "tag_name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `owner` | string | yes | Repository owner or organization login. |
| `repo` | string | yes | Repository name. |
| `tag_name` | string | yes | The name of the tag. |
| `name` | string | no | The name of the release. |
| `body` | string | no | Text describing the contents of the tag. |
| `draft` | boolean | no | Whether to create the release as a draft. |
| `prerelease` | boolean | no | Whether to identify the release as a prerelease. |
| `generate_release_notes` | boolean | no | Whether to automatically generate the release name and body. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `target_commitish` | string | no | The branch or commit SHA where the tag should be created if the tag does not already exist. |
| `discussion_category_name` | string | no | An existing discussion category to create and link to the release. |
| `make_latest` | list<string> | no | Whether this release should be set as the latest release for the repository. One of: `0`, `1`, `2`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GitHub API returns.

## Native endpoint

Through the native GitHub API, this operation is `POST /repos/:owner/:repo/releases` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-release.md) for the provider-specific parameters and requirements.

