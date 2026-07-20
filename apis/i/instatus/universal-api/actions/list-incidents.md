# Instatus: List Incidents



```
GET https://connect.mindcloud.co/v1/universal/instatus/latest/actions/list-incidents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instatus `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instatus/latest/actions/list-incidents?connectionId=$CONNECTION_ID&limit=25&offset=0&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instatus/latest/actions/list-incidents?${params}`, {
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
| `pageId` | string | yes | Instatus status page ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "components": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "id": "string",
      "impact": "string",
      "message": "string",
      "messageHtml": "string",
      "name": "Ava Chen",
      "resolved": "2026-05-07T12:00:00.000Z",
      "started": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updates": [
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
| `components` | array<object> |  |
| `createdAt` | date |  |
| `duration` | number |  |
| `id` | string |  |
| `impact` | string |  |
| `message` | string |  |
| `messageHtml` | string |  |
| `name` | string |  |
| `resolved` | date |  |
| `started` | date |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `updates` | array<object> |  |

## Native endpoint

Through the native Instatus API, this operation is `GET /v1/:page_id/incidents` (base URL `https://api.instatus.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-incidents.md) for the provider-specific parameters and requirements.

