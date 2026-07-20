# Launch27: Create Quote

Creates a new quote in Launch27.

```
POST https://connect.mindcloud.co/v1/universal/launch27/latest/actions/create-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch27 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/launch27/latest/actions/create-quote" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "first_name": "Ava",
  "last_name": "Chen",
  "email": "ava@example.com",
  "phone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/launch27/latest/actions/create-quote', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "first_name": "Ava",
    "last_name": "Chen",
    "email": "ava@example.com",
    "phone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `first_name` | string | yes | Quote requester first name. |
| `last_name` | string | yes | Quote requester last name. |
| `email` | string | yes | Quote requester email address. |
| `phone` | string | yes | Quote requester phone number. |
| `custom_fields` | list<object> | no | Optional Launch27 quote custom fields array. Default: `[]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Launch27 API returns.

## Native endpoint

Through the native Launch27 API, this operation is `POST quote` (base URL `https://{{credentials.subdomain}}.launch27.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-quote.md) for the provider-specific parameters and requirements.

