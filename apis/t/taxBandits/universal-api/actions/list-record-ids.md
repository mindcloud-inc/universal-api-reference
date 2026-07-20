# TaxBandits: List Record IDs

Retrieves record IDs from TaxBandits.

```
GET https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/list-record-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TaxBandits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/list-record-ids?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/list-record-ids?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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
      "Errors": [
        {}
      ],
      "PayerRef": "string",
      "Records": [
        {}
      ],
      "TaxYear": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BusinessId` | string |  |
| `Errors` | array<object> |  |
| `PayerRef` | string |  |
| `Records` | array<object> |  |
| `TaxYear` | string |  |

## Native endpoint

Through the native TaxBandits API, this operation is `GET Utility/GetRecordIds` (base URL `https://testapi.taxbandits.com/v1.7.3/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-record-ids.md) for the provider-specific parameters and requirements.

