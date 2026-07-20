# Hyperise: Create Organization

Creates a client organization in Hyperise.

```
POST https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/create-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/create-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "name": "Ava Chen",
  "seats": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/create-organization', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "name": "Ava Chen",
    "seats": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The invite email for the client organization. |
| `name` | string | yes | The client organization name. |
| `seats` | number | yes | The number of seats to allocate to the client organization. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Hyperise API, this operation is `POST /organizations` (base URL `https://app.hyperise.io/api/v1/regular`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-organization.md) for the provider-specific parameters and requirements.

