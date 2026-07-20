# Spoki: Update Campaign

Updates a campaign by ID, including scheduling, status, or list settings.

```
PUT https://connect.mindcloud.co/v1/universal/spoki/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoki `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/spoki/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spoki/latest/actions/update-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The campaign ID. |
| `name` | string | no | The campaign name. |
| `scheduledDatetime` | date | no | The scheduled send datetime in ISO-8601 format. |
| `status` | string | no | The campaign status. |
| `automation` | number | no | An existing automation ID. |
| `lists[]` | array<number> | no | List IDs included in the campaign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "automation": {},
      "automationCompleted": 1,
      "automationFailed": 1,
      "automationInteractedWith": 1,
      "automationStarted": 1,
      "automationValidFailed": 1,
      "contactsCount": 1,
      "createdDatetime": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "lists": [
        {}
      ],
      "messagesFailed": 1,
      "messagesRead": 1,
      "messagesReceived": 1,
      "messagesSent": 1,
      "name": "Ava Chen",
      "scheduledDatetime": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `automation` | object |  |
| `automationCompleted` | number |  |
| `automationFailed` | number |  |
| `automationInteractedWith` | number |  |
| `automationStarted` | number |  |
| `automationValidFailed` | number |  |
| `contactsCount` | number |  |
| `createdDatetime` | date |  |
| `id` | number |  |
| `lists` | array<object> |  |
| `messagesFailed` | number |  |
| `messagesRead` | number |  |
| `messagesReceived` | number |  |
| `messagesSent` | number |  |
| `name` | string |  |
| `scheduledDatetime` | date |  |
| `status` | string |  |

## Native endpoint

Through the native Spoki API, this operation is `PATCH /campaigns/{{id}}/` (base URL `https://api.spoki.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.

