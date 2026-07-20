# Reward Sciences: Assign External Identity To User



```
POST https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/assign-external-identity-to-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reward Sciences `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/assign-external-identity-to-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": 1,
  "idp": "string",
  "identity": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/assign-external-identity-to-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": 1,
    "idp": "string",
    "identity": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | number | yes | The Reward Sciences user ID. |
| `idp` | string | yes | Identity provider name. |
| `identity` | string | yes | Identity value within the provider. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Reward Sciences API returns.

## Native endpoint

Through the native Reward Sciences API, this operation is `POST /users/:userId/identities` (base URL `https://api.rewardsciences.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-external-identity-to-user.md) for the provider-specific parameters and requirements.

