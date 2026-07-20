# Overledger: Get UTXO State



```
GET https://connect.mindcloud.co/v1/universal/overledger/latest/actions/get-utxo-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Overledger `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/overledger/latest/actions/get-utxo-state?connectionId=$CONNECTION_ID&utxoId=string&location=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "utxoId": "string",
  "location": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/overledger/latest/actions/get-utxo-state?${params}`, {
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
| `utxoId` | string | yes | UTXO identifier to inspect, for example transactionHash:index. |
| `location` | object | yes | Overledger location object with technology and network. Default: `{"network":"Testnet","technology":"Bitcoin"}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "executionUtxoSearchResponse": {},
      "preparationUtxoSearchResponse": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `executionUtxoSearchResponse` | object | UTXO execution details. |
| `preparationUtxoSearchResponse` | object | Preparation response metadata. |

## Native endpoint

Through the native Overledger API, this operation is `POST /v2/autoexecution/search/utxo/:utxoId` (base URL `https://api.overledger.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-utxo-state.md) for the provider-specific parameters and requirements.

