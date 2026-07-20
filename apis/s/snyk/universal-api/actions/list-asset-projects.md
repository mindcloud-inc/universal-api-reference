# Snyk: List Asset Projects

Retrieves projects from a Snyk asset.

```
GET https://connect.mindcloud.co/v1/universal/snyk/latest/actions/list-asset-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snyk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snyk/latest/actions/list-asset-projects?connectionId=$CONNECTION_ID&asset_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "asset_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snyk/latest/actions/list-asset-projects?${params}`, {
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
| `asset_id` | string | yes | Asset ID for the request path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "jsonapi": {},
      "links": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `jsonapi` | object |  |
| `links` | object |  |

## Native endpoint

Through the native Snyk API, this operation is `GET /groups/:group_id/assets/:asset_id/relationships/projects` (base URL `https://api.snyk.io/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-asset-projects.md) for the provider-specific parameters and requirements.

