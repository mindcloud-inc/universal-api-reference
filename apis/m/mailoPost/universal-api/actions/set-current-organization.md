# MailoPost: Set Current Organization

Sets the current organization in MailoPost.

```
PUT https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/set-current-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/set-current-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/set-current-organization', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | MailoPost organization identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "city": "string",
      "country": "string",
      "current": true,
      "id": 1,
      "name": "Ava Chen",
      "phone": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `city` | string |  |
| `country` | string |  |
| `current` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `phone` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native MailoPost API, this operation is `PATCH /email/organizations/:id/current` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-current-organization.md) for the provider-specific parameters and requirements.

