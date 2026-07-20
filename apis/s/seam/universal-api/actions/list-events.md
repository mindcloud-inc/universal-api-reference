# Seam: List Events

Retrieves a list of events from Seam.

```
GET https://connect.mindcloud.co/v1/universal/seam/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seam/latest/actions/list-events?connectionId=$CONNECTION_ID&since=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "since": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seam/latest/actions/list-events?${params}`, {
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
| `connectedAccountId` | string | no | ID of the connected account for which you want to list events. |
| `deviceId` | string | no | ID of the device for which you want to list events. |
| `eventType` | string | no | Type of events that you want to list. |
| `since` | string | yes | Beginning timestamp for the events that you want to list. This action currently requires `since` because `between` is not exposed yet. |

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

Through the native Seam API, this operation is `POST /events/list` (base URL `https://connect.getseam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

