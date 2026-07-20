# Qlik: List Reloads

Retrieves reloads from your Qlik tenant.

```
GET https://connect.mindcloud.co/v1/universal/qlik/latest/actions/list-reloads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qlik `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/list-reloads?connectionId=$CONNECTION_ID&limit=25&offset=0&appId=65b8f2a1f4b0c2d3e4f56789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "appId": "65b8f2a1f4b0c2d3e4f56789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qlik/latest/actions/list-reloads?${params}`, {
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
| `appId` | string | yes | Qlik app ID to list reloads for. Example: `65b8f2a1f4b0c2d3e4f56789`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "appId": "string",
          "endTime": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "startTime": "2026-05-07T12:00:00.000Z",
          "status": "string",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].appId` | string |  |
| `data[].endTime` | date |  |
| `data[].id` | string |  |
| `data[].startTime` | date |  |
| `data[].status` | string |  |
| `data[].type` | string |  |

## Native endpoint

Through the native Qlik API, this operation is `GET /api/v1/reloads` (base URL `https://{{credentials.tenantHost}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-reloads.md) for the provider-specific parameters and requirements.

