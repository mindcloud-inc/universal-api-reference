# Refiner: Identify User

Creates or updates a user in Refiner.

```
POST https://connect.mindcloud.co/v1/universal/refiner/latest/actions/identify-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refiner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/refiner/latest/actions/identify-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/refiner/latest/actions/identify-user', {
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
| `id` | string | no | Identify the user by your own user ID. |
| `email` | string | no | Identify the user by email address. |
| `attributes` | object | no | Additional contact traits to merge into the Refiner contact. |
| `account` | object | no | Optional account object to group multiple contacts under one account. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactUuid": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactUuid` | string | Refiner contact UUID. |
| `message` | string |  |

## Native endpoint

Through the native Refiner API, this operation is `POST /identify-user` (base URL `https://api.refiner.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/identify-user.md) for the provider-specific parameters and requirements.

