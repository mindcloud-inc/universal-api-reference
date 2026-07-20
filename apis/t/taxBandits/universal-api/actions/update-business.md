# TaxBandits: Update Business

Updates an existing business in TaxBandits.

```
PUT https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/update-business
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TaxBandits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/update-business" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/update-business', {
  method: 'PUT',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "BusinessId": "string",
      "BusinessNm": "string",
      "EINorSSN": "string",
      "Errors": [
        {}
      ],
      "IsEIN": true,
      "PayerRef": "string",
      "StatusCode": 1,
      "StatusMessage": "string",
      "StatusName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BusinessId` | string |  |
| `BusinessNm` | string |  |
| `EINorSSN` | string |  |
| `Errors` | array<object> |  |
| `IsEIN` | boolean |  |
| `PayerRef` | string |  |
| `StatusCode` | number |  |
| `StatusMessage` | string |  |
| `StatusName` | string |  |

## Native endpoint

Through the native TaxBandits API, this operation is `PUT Business/Update` (base URL `https://testapi.taxbandits.com/v1.7.3/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-business.md) for the provider-specific parameters and requirements.

