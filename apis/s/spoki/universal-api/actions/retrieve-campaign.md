# Spoki: Retrieve Campaign

Retrieves a campaign by ID.

```
GET https://connect.mindcloud.co/v1/universal/spoki/latest/actions/retrieve-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoki `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoki/latest/actions/retrieve-campaign?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoki/latest/actions/retrieve-campaign?${params}`, {
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
| `id` | number | yes | The campaign ID. |

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

Through the native Spoki API, this operation is `GET /campaigns/{{id}}/` (base URL `https://api.spoki.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-campaign.md) for the provider-specific parameters and requirements.

