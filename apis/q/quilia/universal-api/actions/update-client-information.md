# Quilia: Update Client Information



```
PUT https://connect.mindcloud.co/v1/universal/quilia/latest/actions/update-client-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quilia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/quilia/latest/actions/update-client-information" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quilia/latest/actions/update-client-information', {
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
| `address_1` | string | no | First line of the client's address |
| `address_2` | string | no | Second line of the client's address |
| `city` | string | no | The client's city |
| `country` | string | no | The client's country |
| `email` | string | no | The client's email address |
| `id` | string | yes | The unique identifier of the client to update |
| `language` | string | no | The client's preferred language |
| `name` | string | no | The client's full name |
| `phone` | string | no | The client's phone number |
| `postal_code` | string | no | The client's postal code |
| `state` | string | no | The client's state or province |
| `timezone` | string | no | The client's timezone |
| `date_of_birth` | date | no | The client's date of birth |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Quilia API returns.

## Native endpoint

Through the native Quilia API, this operation is `PATCH clients/:id` (base URL `https://api.quilia.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client-information.md) for the provider-specific parameters and requirements.

