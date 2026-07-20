# Pingdom: Update Contact



```
PUT https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pingdom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": 1,
  "name": "Ava Chen",
  "paused": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": 1,
    "name": "Ava Chen",
    "paused": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | number | yes | Identifier of the contact. |
| `name` | string | yes | Contact name. |
| `paused` | boolean | yes | Pause or unpause notifications for the contact. |
| `notification_targets.email[]` | array<object> | no | Email notification targets as an array of objects with severity and address. |
| `notification_targets.sms[]` | array<object> | no | SMS notification targets as an array of objects with severity, country_code, number, and provider. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "notification_targets": {},
      "owner": true,
      "paused": true,
      "teams": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `notification_targets` | object |  |
| `owner` | boolean |  |
| `paused` | boolean |  |
| `teams` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native Pingdom API, this operation is `PUT /alerting/contacts/:contactid` (base URL `https://api.pingdom.com/api/3.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

