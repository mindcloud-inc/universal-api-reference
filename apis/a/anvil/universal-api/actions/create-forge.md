# Anvil: Create Forge

Creates a new forge in Anvil.

```
POST https://connect.mindcloud.co/v1/universal/anvil/latest/actions/create-forge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anvil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anvil/latest/actions/create-forge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.weldEid": "string",
  "variables.name": "Ava Chen",
  "variables.slug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anvil/latest/actions/create-forge', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.weldEid": "string",
    "variables.name": "Ava Chen",
    "variables.slug": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.weldEid` | string | yes | Provide Weld EID for Create Forge. |
| `variables.name` | string | yes | Provide Name for Create Forge. |
| `variables.slug` | string | yes | Provide Slug for Create Forge. |
| `variables.config` | object | no | Provide Config for Create Forge. |
| `variables.castEid` | string | no | Provide Cast EID for Create Forge. |
| `variables.castFieldIds` | object | no | Provide Cast Field Ids for Create Forge. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Anvil API returns.

## Native endpoint

Through the native Anvil API, this operation is `POST /` (base URL `https://graphql.useanvil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-forge.md) for the provider-specific parameters and requirements.

