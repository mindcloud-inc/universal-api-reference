# Assembly.com: Send Contract

Sends a contract in Assembly.com.

```
POST https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/send-contract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Assembly.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/send-contract" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contractTemplateId": "string",
  "clientId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/send-contract', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contractTemplateId": "string",
    "clientId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contractTemplateId` | string | yes | The unique ID of the contract template the contract is associated with. |
| `clientId` | string | yes | The unique ID of the client receiving the contract request. |
| `companyId` | string | no | The company ID of the client. Required when the client has more than one company. |
| `variableValues` | string | no | A list of fields which represent the specific values for certain contract inputs. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Assembly.com API returns.

## Native endpoint

Through the native Assembly.com API, this operation is `POST /contracts` (base URL `https://api.assembly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-contract.md) for the provider-specific parameters and requirements.

