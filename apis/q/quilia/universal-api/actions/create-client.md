# Quilia: Create Client



```
POST https://connect.mindcloud.co/v1/universal/quilia/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quilia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quilia/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "phone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quilia/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "phone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address_1` | string | no | The first line of the address |
| `address_2` | string | no | The second line of the address |
| `city` | string | no | The city |
| `country` | string | no | The country |
| `email` | string | no | The email of the client |
| `language_code` | string | no | The language code of the client |
| `name` | string | yes | The name of the client |
| `name_first` | string | no | The first name of the client |
| `name_last` | string | no | The last name of the client |
| `postal_code` | string | no | The postal code |
| `state` | string | no | The state or province |
| `phone` | string | yes | The phone number of the client |
| `date_of_birth` | date | no | The date of birth in YYYY-MM-DD format |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Quilia API returns.

## Native endpoint

Through the native Quilia API, this operation is `POST clients` (base URL `https://api.quilia.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

