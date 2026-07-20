# Instatus: Get Incident Update



```
GET https://connect.mindcloud.co/v1/universal/instatus/latest/actions/get-incident-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instatus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instatus/latest/actions/get-incident-update?connectionId=$CONNECTION_ID&pageId=string&incidentId=string&incidentUpdateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageId": "string",
  "incidentId": "string",
  "incidentUpdateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instatus/latest/actions/get-incident-update?${params}`, {
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
| `incidentId` | string | yes | Instatus incident ID. |
| `incidentUpdateId` | string | yes | Instatus incident update ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "ended": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "incidentId": "string",
      "message": "string",
      "messageHtml": "string",
      "notify": true,
      "started": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `duration` | number |  |
| `ended` | date |  |
| `id` | string |  |
| `incidentId` | string |  |
| `message` | string |  |
| `messageHtml` | string |  |
| `notify` | boolean |  |
| `started` | date |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Instatus API, this operation is `GET /v1/:page_id/incidents/:incident_id/incident-updates/:incident_update_id` (base URL `https://api.instatus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-incident-update.md) for the provider-specific parameters and requirements.

