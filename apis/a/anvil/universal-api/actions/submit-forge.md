# Anvil: Submit Forge

Submits data to a Forge webform in Anvil.

```
POST https://connect.mindcloud.co/v1/universal/anvil/latest/actions/submit-forge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anvil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anvil/latest/actions/submit-forge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.forgeEid": "string",
  "variables.payload": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anvil/latest/actions/submit-forge', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.forgeEid": "string",
    "variables.payload": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.forgeEid` | string | yes | Provide Forge EID for Submit Forge. |
| `variables.weldDataEid` | string | no | Provide Weld Data EID for Submit Forge. |
| `variables.submissionEid` | string | no | Provide Submission EID for Submit Forge. |
| `variables.payload` | object | yes | Provide Payload for Submit Forge. |
| `variables.enforcePayloadValidOnCreate` | boolean | no | Provide Enforce Payload Valid On Create for Submit Forge. |
| `variables.currentStep` | number | no | Provide Current Step for Submit Forge. |
| `variables.complete` | boolean | no | Provide Complete for Submit Forge. |
| `variables.isTest` | boolean | no | Provide Is Test for Submit Forge. |
| `variables.timezone` | string | no | Provide Timezone for Submit Forge. |
| `variables.webhookURL` | string | no | Provide Webhook URL for Submit Forge. |
| `variables.groupArrayId` | string | no | Provide Group Array ID for Submit Forge. |
| `variables.groupArrayIndex` | number | no | Provide Group Array Index for Submit Forge. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Anvil API returns.

## Native endpoint

Through the native Anvil API, this operation is `POST /` (base URL `https://graphql.useanvil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-forge.md) for the provider-specific parameters and requirements.

