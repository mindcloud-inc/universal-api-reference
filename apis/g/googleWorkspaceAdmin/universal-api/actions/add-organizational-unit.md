# Google Workspace Admin: Add Organizational Unit

Creates an organizational unit in Google Workspace Admin.

```
POST https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/add-organizational-unit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Workspace Admin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/add-organizational-unit" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "my_customer",
  "name": "Ava Chen",
  "parentOrgUnitPath": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/add-organizational-unit', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "my_customer",
    "name": "Ava Chen",
    "parentOrgUnitPath": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | yes | Workspace customer identifier. Use my_customer for the current tenant. Default: `my_customer`. |
| `description` | string | no | Optional description for the organizational unit. |
| `name` | string | yes | Name of the new organizational unit. |
| `parentOrgUnitPath` | string | yes | Parent organizational unit path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "etag": "string",
      "kind": "string",
      "name": "Ava Chen",
      "orgUnitId": "string",
      "orgUnitPath": "string",
      "parentOrgUnitId": "string",
      "parentOrgUnitPath": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `etag` | string |  |
| `kind` | string |  |
| `name` | string |  |
| `orgUnitId` | string |  |
| `orgUnitPath` | string |  |
| `parentOrgUnitId` | string |  |
| `parentOrgUnitPath` | string |  |

## Native endpoint

Through the native Google Workspace Admin API, this operation is `POST /admin/directory/v1/customer/:customerId/orgunits` (base URL `https://admin.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-organizational-unit.md) for the provider-specific parameters and requirements.

