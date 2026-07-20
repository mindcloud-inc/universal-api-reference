# Overledger: Read Smart Contract Function



```
GET https://connect.mindcloud.co/v1/universal/overledger/latest/actions/read-smart-contract-function
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Overledger `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/overledger/latest/actions/read-smart-contract-function?connectionId=$CONNECTION_ID&location=%5Bobject%20Object%5D&functionName=Ava%20Chen&smartContractId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "location": "[object Object]",
  "functionName": "Ava Chen",
  "smartContractId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/overledger/latest/actions/read-smart-contract-function?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `location` | object | yes | Overledger location object with technology and network. Default: `{"network":"ethereum sepolia testnet","technology":"ethereum"}`. |
| `functionName` | string | yes | Smart contract read function name. |
| `smartContractId` | string | yes | Smart contract identifier/address. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inputParameters[]` | array<object> | no | Optional array of smart contract input parameter objects with type and value. |
| `outputParameters[]` | array<object> | no | Optional array of smart contract output parameter objects with type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "functionName": "Ava Chen",
      "location": {},
      "outputParameters": [
        {}
      ],
      "smartContractId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `functionName` | string | Read function name. |
| `location` | object | Blockchain location. |
| `outputParameters` | array<object> | Returned output parameters. |
| `smartContractId` | string | Smart contract identifier. |

## Native endpoint

Through the native Overledger API, this operation is `POST /api/smart-contracts/read` (base URL `https://api.overledger.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-smart-contract-function.md) for the provider-specific parameters and requirements.

