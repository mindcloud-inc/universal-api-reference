# MailoPost: Create Organization

Creates a new organization in MailoPost.

```
POST https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/create-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/create-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "address": "string",
  "country": "string",
  "city": "string",
  "phone": "string",
  "zip": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/create-organization', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "address": "string",
    "country": "string",
    "city": "string",
    "phone": "string",
    "zip": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Organization name. |
| `address` | string | yes | Organization address. |
| `country` | string | yes | Organization country. |
| `city` | string | yes | Organization city. |
| `phone` | string | yes | Organization phone number. |
| `zip` | string | yes | Organization postal code. |

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

Through the native MailoPost API, this operation is `POST /email/organizations` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-organization.md) for the provider-specific parameters and requirements.

