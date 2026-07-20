# SimFin: Download Germany TTM bank cashflow dataset

Retrieves the Germany TTM bank cashflow dataset from SimFin.

```
GET https://connect.mindcloud.co/v1/universal/simFin/latest/actions/download-germany-ttm-bank-cashflow-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimFin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simFin/latest/actions/download-germany-ttm-bank-cashflow-dataset?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simFin/latest/actions/download-germany-ttm-bank-cashflow-dataset?${params}`, {
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
      "downloaded": true,
      "market": "string",
      "variant": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataset` | string | SimFin dataset key requested from the bulk-download API. |
| `downloaded` | boolean | Whether the dataset download request was configured successfully. |
| `market` | string | Market code requested for market-scoped datasets. |
| `variant` | string | Dataset variant when applicable. |

## Native endpoint

Through the native SimFin API, this operation is `GET s3?dataset=cashflow-banks&variant=ttm&market=de` (base URL `https://prod.simfin.com/api/bulk-download`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-germany-ttm-bank-cashflow-dataset.md) for the provider-specific parameters and requirements.

