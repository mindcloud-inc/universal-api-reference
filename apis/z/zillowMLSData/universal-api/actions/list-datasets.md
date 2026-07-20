# Zillow MLS Data: List datasets

Retrieves available datasets from Zillow MLS Data.

```
GET https://connect.mindcloud.co/v1/universal/zillowMLSData/latest/actions/list-datasets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zillow MLS Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowMLSData/latest/actions/list-datasets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zillowMLSData/latest/actions/list-datasets?${params}`, {
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
      "datasetCode": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datasetCode` | string | Bridge dataset code. |
| `description` | string | Dataset description. |
| `id` | string | Unique dataset identifier. |
| `name` | string | Dataset name. |

## Native endpoint

Through the native Zillow MLS Data API, this operation is `GET /datasets` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-datasets.md) for the provider-specific parameters and requirements.

