# xMatters: Change the status of an event

Changes the status of an event in your xMatters instance.

```
PUT https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/change-the-status-of-an-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/change-the-status-of-an-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/change-the-status-of-an-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no |  |
| `status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bypassPhoneIntro": true,
      "created": "2026-05-07T12:00:00.000Z",
      "escalationOverride": true,
      "eventId": "string",
      "id": "string",
      "incident": "string",
      "links": {
        "self": "https://example.com"
      },
      "overrideDeviceRestrictions": true,
      "priority": "string",
      "requirePhonePassword": true,
      "status": "string",
      "submitter": {
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "links": {
          "self": "https://example.com"
        },
        "recipientType": "string",
        "targetName": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bypassPhoneIntro` | boolean |  |
| `created` | date |  |
| `escalationOverride` | boolean |  |
| `eventId` | string |  |
| `id` | string |  |
| `incident` | string |  |
| `links.self` | string |  |
| `overrideDeviceRestrictions` | boolean |  |
| `priority` | string |  |
| `requirePhonePassword` | boolean |  |
| `status` | string |  |
| `submitter.firstName` | string |  |
| `submitter.id` | string |  |
| `submitter.lastName` | string |  |
| `submitter.links.self` | string |  |
| `submitter.recipientType` | string |  |
| `submitter.targetName` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `POST events` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-the-status-of-an-event.md) for the provider-specific parameters and requirements.

