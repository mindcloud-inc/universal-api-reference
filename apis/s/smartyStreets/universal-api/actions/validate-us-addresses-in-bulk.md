# Smarty-streets: Validate US Addresses In Bulk

Retrieves validated US addresses from Smarty-streets in bulk.

```
GET https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/validate-us-addresses-in-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smarty-streets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/validate-us-addresses-in-bulk?connectionId=$CONNECTION_ID&addresses%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "addresses[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/validate-us-addresses-in-bulk?${params}`, {
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
| `addresses[]` | array<object> | yes | Array of US address lookup objects. Default: `[{"city":"North Pole","state":"AK","street":"1 Santa Claus Ln"}]`. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analysis": {},
      "candidateIndex": 1,
      "components": {},
      "deliveryLine1": "string",
      "inputIndex": 1,
      "lastLine": "string",
      "metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analysis` | object |  |
| `candidateIndex` | number |  |
| `components` | object |  |
| `deliveryLine1` | string |  |
| `inputIndex` | number |  |
| `lastLine` | string |  |
| `metadata` | object |  |

## Native endpoint

Through the native Smarty-streets API, this operation is `POST https://us-street.api.smarty.com/street-address` (base URL `https://us-street.api.smarty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-us-addresses-in-bulk.md) for the provider-specific parameters and requirements.

