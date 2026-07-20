# Mobile Text Alerts: Update Subscriber

Updates an existing subscriber in Mobile Text Alerts.

```
PUT https://connect.mindcloud.co/v1/universal/mobileTextAlerts/latest/actions/update-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mobile Text Alerts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mobileTextAlerts/latest/actions/update-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idOrNumberOrEmail": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mobileTextAlerts/latest/actions/update-subscriber', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "idOrNumberOrEmail": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idOrNumberOrEmail` | string | yes | Subscriber ID, phone number, or email. |
| `email` | string | no | Updated subscriber email address. |
| `number` | string | no | Updated subscriber phone number. |
| `firstName` | string | no | Updated subscriber first name. |
| `lastName` | string | no | Updated subscriber last name. |
| `groupIds` | string | no | Comma-separated Mobile Text Alerts group IDs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Updated subscriber returned by Mobile Text Alerts. |
| `message` | string | Optional API response message. |

## Native endpoint

Through the native Mobile Text Alerts API, this operation is `PATCH /subscribers/:idOrNumberOrEmail` (base URL `https://api.mobile-text-alerts.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscriber.md) for the provider-specific parameters and requirements.

