# Kit: Update Subscriber

Updates an existing subscriber in Kit.

```
PUT https://connect.mindcloud.co/v1/universal/kit/latest/actions/update-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kit/latest/actions/update-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kit/latest/actions/update-subscriber', {
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
| `id` | number | yes | Subscriber ID. |
| `emailAddress` | string | no | Updated subscriber email address. |
| `state` | list<string> | no | Updated subscriber state. One of: `active`, `bounced`, `cancelled`, `complained`, `inactive`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "subscriber": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "email_address": "ava@example.com",
        "fields": {},
        "first_name": "Ava",
        "id": 1,
        "state": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `subscriber` | object |  |
| `subscriber.created_at` | date |  |
| `subscriber.email_address` | string |  |
| `subscriber.fields` | object |  |
| `subscriber.first_name` | string |  |
| `subscriber.id` | number |  |
| `subscriber.state` | string |  |

## Native endpoint

Through the native Kit API, this operation is `PUT /subscribers/:id` (base URL `https://api.kit.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscriber.md) for the provider-specific parameters and requirements.

