# Planyo: Update User

Updates an existing user in Planyo.

```
PUT https://connect.mindcloud.co/v1/universal/planyo/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planyo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/planyo/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/planyo/latest/actions/update-user', {
  method: 'PUT',
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
| `userId` | number | no |  |
| `email` | string | no |  |
| `userLogin` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `newEmail` | string | no |  |
| `emailVerified` | boolean | no |  |
| `city` | string | no |  |
| `country` | string | no |  |
| `userLanguage` | string | no |  |
| `isPreapproved` | boolean | no |  |
| `isBanned` | boolean | no |  |
| `siteId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `userId` | number |  |

## Native endpoint

Through the native Planyo API, this operation is `GET /` (base URL `https://www.planyo.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

