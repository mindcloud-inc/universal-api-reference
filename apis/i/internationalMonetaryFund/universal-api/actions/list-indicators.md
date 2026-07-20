# International Monetary Fund: List Indicators

Retrieves available indicators from the IMF DataMapper API.

```
GET https://connect.mindcloud.co/v1/universal/internationalMonetaryFund/latest/actions/list-indicators
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a International Monetary Fund `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/internationalMonetaryFund/latest/actions/list-indicators?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/internationalMonetaryFund/latest/actions/list-indicators?${params}`, {
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
      "dataset": "string",
      "description": "string",
      "id": "string",
      "label": "string",
      "source": "string",
      "unit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataset` | string | Dataset code. |
| `description` | string | Indicator description. |
| `id` | string | Indicator identifier. |
| `label` | string | Indicator display name. |
| `source` | string | Source dataset or publication. |
| `unit` | string | Measurement unit. |

## Native endpoint

Through the native International Monetary Fund API, this operation is `GET /indicators` (base URL `https://www.imf.org/external/datamapper/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-indicators.md) for the provider-specific parameters and requirements.

