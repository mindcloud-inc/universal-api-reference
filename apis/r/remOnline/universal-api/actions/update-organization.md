# RemOnline: Update Organization

Updates an existing organization in RemOnline.

```
PUT https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/update-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RemOnline `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/update-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organization_id": "38077744"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/update-organization', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organization_id": "38077744"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organization_id` | number | yes | ID of the organization. Example: `38077744`. |
| `notes` | string | no | Notes text. Example: `Updated by MindCloud Stage3`. |
| `name` | string | no | Organization name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RemOnline API returns.

## Native endpoint

Through the native RemOnline API, this operation is `PATCH /v2/contacts/organizations/:organization_id` (base URL `https://api.roapp.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-organization.md) for the provider-specific parameters and requirements.

