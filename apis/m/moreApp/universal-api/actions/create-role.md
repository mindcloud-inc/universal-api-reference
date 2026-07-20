# MoreApp: Create Role

Creates a role in MoreApp.

```
POST https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/create-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/create-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/create-role', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes |  |
| `name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": {},
      "message": "string",
      "scope": "string",
      "status": 1,
      "traceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | object | Additional provider error details when present. |
| `message` | string | Provider message describing the role creation restriction. |
| `scope` | string | MoreApp error scope for the create role response. |
| `status` | number | HTTP-style provider status returned when role creation is blocked. |
| `traceId` | string | MoreApp trace identifier for support and debugging. |

## Native endpoint

Through the native MoreApp API, this operation is `POST /api/v2/customers/{{customerId}}/roles` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-role.md) for the provider-specific parameters and requirements.

