# RotaCloud: Create Onboarding Request



```
POST https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-onboarding-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-onboarding-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "locations[]": [
    1
  ],
  "users[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-onboarding-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "locations[]": [1],
    "users[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locations[]` | array<number> | yes | Location IDs for onboarding. |
| `users[]` | array<object> | yes | Pending users to onboard. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "locations": [
        1
      ],
      "users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `locations` | array<number> |  |
| `users` | array<object> |  |

## Native endpoint

Through the native RotaCloud API, this operation is `POST /v2/users/onboard` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-onboarding-request.md) for the provider-specific parameters and requirements.

