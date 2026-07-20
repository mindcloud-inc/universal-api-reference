# Deepset: Get Query Sets

Retrieves query sets from a Deepset workspace.

```
GET https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-query-sets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-query-sets?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-query-sets?${params}`, {
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
| `workspaceId` | string | yes | deepset workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "query_set_id": "string"
        }
      ],
      "has_more": true,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].created_at` | date |  |
| `data[].name` | string |  |
| `data[].query_set_id` | string |  |
| `has_more` | boolean |  |
| `total` | number |  |

## Native endpoint

Through the native Deepset API, this operation is `GET /api/v2/workspaces/:workspace_id/query_sets` (base URL `https://api.cloud.deepset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-query-sets.md) for the provider-specific parameters and requirements.

