# Anvil: Create Weld

Creates a new weld in Anvil.

```
POST https://connect.mindcloud.co/v1/universal/anvil/latest/actions/create-weld
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anvil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anvil/latest/actions/create-weld" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anvil/latest/actions/create-weld', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.organizationEid` | string | no | Provide Organization EID for Create Weld. |
| `variables.name` | string | no | Provide Name for Create Weld. |
| `variables.slug` | string | no | Provide Slug for Create Weld. |
| `variables.visibility` | string | no | Provide Visibility for Create Weld. |
| `variables.draftStep` | string | no | Provide Draft Step for Create Weld. |
| `variables.config` | object | no | Provide Config for Create Weld. |
| `variables.castEid` | string | no | Provide Cast EID for Create Weld. |
| `variables.files[]` | array<object> | no | Provide Files for Create Weld. |
| `variables.createCastTemplatesFromUploads` | boolean | no | Provide Create Cast Templates From Uploads for Create Weld. |
| `variables.advancedCreate` | boolean | no | Provide Advanced Create for Create Weld. |
| `variables.advancedDetectFields` | boolean | no | Provide Advanced Detect Fields for Create Weld. |
| `variables.detectBoxesAdvanced` | boolean | no | Provide Detect Boxes Advanced for Create Weld. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Anvil API returns.

## Native endpoint

Through the native Anvil API, this operation is `POST /` (base URL `https://graphql.useanvil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-weld.md) for the provider-specific parameters and requirements.

