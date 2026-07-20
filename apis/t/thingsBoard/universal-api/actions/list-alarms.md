# ThingsBoard: List Alarms

Retrieves alarms for a specific entity from ThingsBoard.

```
GET https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/list-alarms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThingsBoard `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/list-alarms?connectionId=$CONNECTION_ID&limit=25&offset=0&entityType=string&entityId=string&pageSize=1&page=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "entityType": "string",
  "entityId": "string",
  "pageSize": "1",
  "page": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/list-alarms?${params}`, {
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
| `entityType` | string | yes | The ThingsBoard entity type, for example DEVICE. |
| `entityId` | string | yes | The ThingsBoard entity ID. |
| `pageSize` | number | yes | Maximum number of alarms to return in one page. |
| `page` | number | yes | Zero-based page number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "acknowledged": true,
          "cleared": true,
          "createdTime": 1,
          "id": {
            "entityType": "string",
            "id": "string"
          },
          "originator": {
            "entityType": "string",
            "id": "string"
          },
          "severity": "string",
          "type": "string"
        }
      ],
      "hasNext": true,
      "totalElements": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].acknowledged` | boolean |  |
| `data[].cleared` | boolean |  |
| `data[].createdTime` | number |  |
| `data[].id.entityType` | string |  |
| `data[].id.id` | string |  |
| `data[].originator.entityType` | string |  |
| `data[].originator.id` | string |  |
| `data[].severity` | string |  |
| `data[].type` | string |  |
| `hasNext` | boolean |  |
| `totalElements` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native ThingsBoard API, this operation is `GET /alarm/:entityType/:entityId` (base URL `{{credentials.baseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-alarms.md) for the provider-specific parameters and requirements.

