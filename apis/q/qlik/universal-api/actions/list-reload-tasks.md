# Qlik: List Reload Tasks

Retrieves reload tasks from your Qlik tenant.

```
GET https://connect.mindcloud.co/v1/universal/qlik/latest/actions/list-reload-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qlik `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/list-reload-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qlik/latest/actions/list-reload-tasks?${params}`, {
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
| `appId` | string | no | Optional Qlik app ID to filter reload tasks. Example: `65b8f2a1f4b0c2d3e4f56789`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "appId": "string",
          "enabled": true,
          "id": "string",
          "partial": true,
          "spaceId": "string"
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
| `data[].enabled` | boolean |  |
| `data[].id` | string |  |
| `data[].partial` | boolean |  |
| `data[].spaceId` | string |  |

## Native endpoint

Through the native Qlik API, this operation is `GET /api/v1/reload-tasks` (base URL `https://{{credentials.tenantHost}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-reload-tasks.md) for the provider-specific parameters and requirements.

