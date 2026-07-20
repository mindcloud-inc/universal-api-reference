# Sarbacane: Create SMS Campaign

Creates a new SMS campaign in Sarbacane.

```
POST https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/create-sms-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sarbacane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/create-sms-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/create-sms-campaign', {
  method: 'POST',
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
| `content` | string | no | SMS content. |
| `kind` | string | no | SMS campaign kind: SMS_MARKETING or SMS_NOTIFICATION. |
| `name` | string | no | Campaign name. |
| `smsFrom` | string | no | Optional SMS sender name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created campaign ID. |
| `name` | string | Campaign name. |

## Native endpoint

Through the native Sarbacane API, this operation is `POST /campaigns/sms` (base URL `https://api.sarbacane.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sms-campaign.md) for the provider-specific parameters and requirements.

