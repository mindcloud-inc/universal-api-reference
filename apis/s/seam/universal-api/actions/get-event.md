# Seam: Get Event

Retrieves an event from Seam.

```
GET https://connect.mindcloud.co/v1/universal/seam/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seam/latest/actions/get-event?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seam/latest/actions/get-event?${params}`, {
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
| `deviceId` | string | no | Unique identifier for the device that triggered the event that you want to get. |
| `eventId` | string | no | Unique identifier for the event that you want to get. |
| `eventType` | string | no | Type of the event that you want to get. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connectedAccountCustomMetadata": {},
      "connectedAccountId": "string",
      "connectWebviewId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deviceCustomMetadata": {},
      "deviceId": "string",
      "eventDescription": "string",
      "eventId": "string",
      "eventType": "string",
      "occurredAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connectedAccountCustomMetadata` | object |  |
| `connectedAccountId` | string |  |
| `connectWebviewId` | string |  |
| `createdAt` | date |  |
| `deviceCustomMetadata` | object |  |
| `deviceId` | string |  |
| `eventDescription` | string |  |
| `eventId` | string |  |
| `eventType` | string |  |
| `occurredAt` | date |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Seam API, this operation is `POST /events/get` (base URL `https://connect.getseam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

