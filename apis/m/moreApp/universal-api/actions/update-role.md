# MoreApp: Update Role

Updates a role in MoreApp.

```
PUT https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/update-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/update-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "roleId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/update-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "roleId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes |  |
| `roleId` | string | yes |  |
| `name` | string | no |  |

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
| `message` | string | Provider message describing the role update restriction. |
| `scope` | string | MoreApp error scope for the update role response. |
| `status` | number | HTTP-style provider status returned when role updates are blocked. |
| `traceId` | string | MoreApp trace identifier for support and debugging. |

## Native endpoint

Through the native MoreApp API, this operation is `PATCH /api/v2/customers/{{customerId}}/roles/{{roleId}}` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-role.md) for the provider-specific parameters and requirements.

