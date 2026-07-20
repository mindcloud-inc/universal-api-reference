# Reward Sciences: Create User By External Identity



```
POST https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/create-user-by-external-identity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reward Sciences `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/create-user-by-external-identity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idp": "string",
  "identity": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/create-user-by-external-identity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `idp` | string | yes | Identity provider name. |
| `identity` | string | yes | Identity value within the provider. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `user_id` | number | Created Reward Sciences user ID. |

## Native endpoint

Through the native Reward Sciences API, this operation is `POST /idps/:idp/:identity/user` (base URL `https://api.rewardsciences.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user-by-external-identity.md) for the provider-specific parameters and requirements.

