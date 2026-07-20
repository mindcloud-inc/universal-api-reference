# Instatus: List Maintenances



```
GET https://connect.mindcloud.co/v1/universal/instatus/latest/actions/list-maintenances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instatus `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instatus/latest/actions/list-maintenances?connectionId=$CONNECTION_ID&limit=25&offset=0&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instatus/latest/actions/list-maintenances?${params}`, {
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
      "autoEnd": true,
      "autoStart": true,
      "components": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "end": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "impact": "string",
      "message": "string",
      "messageHtml": "string",
      "name": "Ava Chen",
      "notify": true,
      "notifyEarly": true,
      "notifyEnd": true,
      "notifyStart": true,
      "siteId": "string",
      "start": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "translations": {},
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
| `autoEnd` | boolean |  |
| `autoStart` | boolean |  |
| `components` | array<object> |  |
| `createdAt` | date |  |
| `duration` | number |  |
| `end` | date |  |
| `id` | string |  |
| `impact` | string |  |
| `message` | string |  |
| `messageHtml` | string |  |
| `name` | string |  |
| `notify` | boolean |  |
| `notifyEarly` | boolean |  |
| `notifyEnd` | boolean |  |
| `notifyStart` | boolean |  |
| `siteId` | string |  |
| `start` | date |  |
| `status` | string |  |
| `translations` | object |  |
| `updatedAt` | date |  |
| `updates` | array<object> |  |

## Native endpoint

Through the native Instatus API, this operation is `GET /v1/:page_id/maintenances` (base URL `https://api.instatus.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-maintenances.md) for the provider-specific parameters and requirements.

