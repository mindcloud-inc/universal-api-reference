# Overledger: Get Address Sequence



```
GET https://connect.mindcloud.co/v1/universal/overledger/latest/actions/get-address-sequence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Overledger `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/overledger/latest/actions/get-address-sequence?connectionId=$CONNECTION_ID&addressId=string&location=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "addressId": "string",
  "location": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/overledger/latest/actions/get-address-sequence?${params}`, {
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
| `addressId` | string | yes | Blockchain address whose sequence/nonce should be retrieved. |
| `location` | object | yes | Overledger location object with technology and network. Default: `{"network":"ethereum sepolia testnet","technology":"ethereum"}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "executionAddressSequenceSearchResponse": {},
      "preparationAddressSequenceSearchResponse": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `executionAddressSequenceSearchResponse` | object | Address sequence execution details. |
| `preparationAddressSequenceSearchResponse` | object | Preparation response metadata. |

## Native endpoint

Through the native Overledger API, this operation is `POST /v2/autoexecution/search/address/sequence/:addressId` (base URL `https://api.overledger.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-address-sequence.md) for the provider-specific parameters and requirements.

