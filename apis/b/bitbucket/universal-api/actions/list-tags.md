# Bitbucket: List Tags

Retrieves tags from Bitbucket.

```
GET https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitbucket `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/list-tags?connectionId=$CONNECTION_ID&limit=25&offset=0&workspace=mindcloudbitbucket20260409&repo_slug=mindcloud-validation-repo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspace": "mindcloudbitbucket20260409",
  "repo_slug": "mindcloud-validation-repo"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/list-tags?${params}`, {
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
| `workspace` | string | yes | Workspace slug. Default: `mindcloudbitbucket20260409`. |
| `repo_slug` | string | yes | Repository slug. Default: `mindcloud-validation-repo`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "next": "string",
      "page": 1,
      "pagelen": 1,
      "previous": "string",
      "size": 1,
      "values": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `next` | string |  |
| `page` | number |  |
| `pagelen` | number |  |
| `previous` | string |  |
| `size` | number |  |
| `values` | array<object> |  |

## Native endpoint

Through the native Bitbucket API, this operation is `GET /repositories/:workspace/:repo_slug/refs/tags` (base URL `https://api.bitbucket.org/2.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

