# WebAutomation.io: Update Extractor Variables

Updates one variable value for a specific extractor.

```
PUT https://connect.mindcloud.co/v1/universal/webAutomationio/latest/actions/update-extractor-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebAutomation.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/webAutomationio/latest/actions/update-extractor-variables" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "extractorId": 1,
  "variableKey": "string",
  "variableValue": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webAutomationio/latest/actions/update-extractor-variables', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "extractorId": 1,
    "variableKey": "string",
    "variableValue": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `extractorId` | number | yes | The extractor ID. |
| `fieldType` | string | no | The extractor variable field type. |
| `variableKey` | string | yes | The extractor variable key to update. |
| `variableValue` | string | yes | The value to assign to the extractor variable. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WebAutomation.io API returns.

## Native endpoint

Through the native WebAutomation.io API, this operation is `PUT /extractor_variables/{{EXTRACTOR_ID}}/` (base URL `https://webautomation.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-extractor-variables.md) for the provider-specific parameters and requirements.

