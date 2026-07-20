# MoreApp: Update Invite Grant

Updates an invite's grants in MoreApp.

```
PUT https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/update-invite-grant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/update-invite-grant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "id": "string",
  "operation": "string",
  "resourceId": "string",
  "resourceType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/update-invite-grant', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "id": "string",
    "operation": "string",
    "resourceId": "string",
    "resourceType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes |  |
| `roleId` | string | no |  |
| `id` | string | yes |  |
| `operation` | string | yes |  |
| `resourceId` | string | yes |  |
| `resourceType` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerId": 1,
      "resourceId": "string",
      "resourceType": "string",
      "roleId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerId` | number |  |
| `resourceId` | string |  |
| `resourceType` | string |  |
| `roleId` | string |  |

## Native endpoint

Through the native MoreApp API, this operation is `PATCH /api/v2/customers/{{customerId}}/invites/{{id}}/grants` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invite-grant.md) for the provider-specific parameters and requirements.

