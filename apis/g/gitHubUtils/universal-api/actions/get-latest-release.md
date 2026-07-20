# GitHub Utils: Get Latest Release

Retrieves the latest release from a GitHub repository.

```
GET https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/get-latest-release
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub Utils `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/get-latest-release?connectionId=$CONNECTION_ID&owner=string&repo=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "owner": "string",
  "repo": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/get-latest-release?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `owner` | string | yes | Repository owner or organization login. |
| `repo` | string | yes | Repository name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assets": [
        {}
      ],
      "assets_url": "https://example.com",
      "author": {},
      "body": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "draft": true,
      "html_url": "https://example.com",
      "id": 1,
      "immutable": true,
      "name": "Ava Chen",
      "node_id": "string",
      "prerelease": true,
      "published_at": "2026-05-07T12:00:00.000Z",
      "tag_name": "Ava Chen",
      "tarball_url": "https://example.com",
      "target_commitish": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "upload_url": "https://example.com",
      "url": "https://example.com",
      "zipball_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assets` | array<object> |  |
| `assets_url` | string |  |
| `author` | object |  |
| `body` | string |  |
| `created_at` | date |  |
| `draft` | boolean |  |
| `html_url` | string |  |
| `id` | number |  |
| `immutable` | boolean |  |
| `name` | string |  |
| `node_id` | string |  |
| `prerelease` | boolean |  |
| `published_at` | date |  |
| `tag_name` | string |  |
| `tarball_url` | string |  |
| `target_commitish` | string |  |
| `updated_at` | date |  |
| `upload_url` | string |  |
| `url` | string |  |
| `zipball_url` | string |  |

## Native endpoint

Through the native GitHub Utils API, this operation is `GET /repos/:owner/:repo/releases/latest` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest-release.md) for the provider-specific parameters and requirements.

