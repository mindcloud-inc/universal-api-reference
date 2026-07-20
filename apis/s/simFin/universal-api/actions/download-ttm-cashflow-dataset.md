# SimFin: Download TTM cashflow dataset

Retrieves the TTM cashflow dataset from SimFin.

```
GET https://connect.mindcloud.co/v1/universal/simFin/latest/actions/download-ttm-cashflow-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimFin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simFin/latest/actions/download-ttm-cashflow-dataset?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simFin/latest/actions/download-ttm-cashflow-dataset?${params}`, {
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
| `dataset` | string |  |
| `downloaded` | boolean |  |
| `market` | string |  |
| `variant` | string |  |

## Native endpoint

Through the native SimFin API, this operation is `GET s3?dataset=cashflow&variant=ttm&market=us` (base URL `https://prod.simfin.com/api/bulk-download`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-ttm-cashflow-dataset.md) for the provider-specific parameters and requirements.

