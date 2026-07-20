# RotaCloud: Create Users Onboarding Batch V2



```
POST https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-users-onboarding-batch-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-users-onboarding-batch-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "users[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-users-onboarding-batch-v2', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "users[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `users[]` | array<object> | yes | Users payload for batch v2 create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "level": "string",
      "locations": [
        1
      ],
      "roles": [
        {}
      ],
      "salary": 1,
      "salaryType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `level` | string |  |
| `locations` | array<number> |  |
| `roles` | array<object> |  |
| `salary` | number |  |
| `salaryType` | string |  |

## Native endpoint

Through the native RotaCloud API, this operation is `POST /v2/users` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-users-onboarding-batch-v2.md) for the provider-specific parameters and requirements.

