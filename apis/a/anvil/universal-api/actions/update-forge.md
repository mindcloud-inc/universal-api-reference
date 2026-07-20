# Anvil: Update Forge

Updates an existing forge in Anvil.

```
PUT https://connect.mindcloud.co/v1/universal/anvil/latest/actions/update-forge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anvil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/anvil/latest/actions/update-forge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.eid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anvil/latest/actions/update-forge', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.eid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.eid` | string | yes | Provide EID for Update Forge. |
| `variables.name` | string | no | Provide Name for Update Forge. |
| `variables.slug` | string | no | Provide Slug for Update Forge. |
| `variables.config` | object | no | Provide Config for Update Forge. |
| `variables.configFile` | file | no | Provide Config File for Update Forge. |
| `variables.isArchived` | boolean | no | Provide Is Archived for Update Forge. |
| `variables.isRequired` | boolean | no | Provide Is Required for Update Forge. |
| `variables.title` | string | no | Provide Title for Update Forge. |
| `variables.organizationRole` | string | no | Provide Organization Role for Update Forge. |
| `variables.unauthenticatedAuthType` | string | no | Provide Unauthenticated Auth Type for Update Forge. |
| `variables.versionNumber` | number | no | Provide Version Number for Update Forge. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Anvil API returns.

## Native endpoint

Through the native Anvil API, this operation is `POST /` (base URL `https://graphql.useanvil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-forge.md) for the provider-specific parameters and requirements.

