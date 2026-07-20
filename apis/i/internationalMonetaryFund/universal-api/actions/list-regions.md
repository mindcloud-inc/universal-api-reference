# International Monetary Fund: List Regions

Retrieves defined regions from the IMF DataMapper API.

```
GET https://connect.mindcloud.co/v1/universal/internationalMonetaryFund/latest/actions/list-regions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a International Monetary Fund `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/internationalMonetaryFund/latest/actions/list-regions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/internationalMonetaryFund/latest/actions/list-regions?${params}`, {
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
      "id": "string",
      "label": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Region identifier. |
| `label` | string | Region name. |

## Native endpoint

Through the native International Monetary Fund API, this operation is `GET /regions` (base URL `https://www.imf.org/external/datamapper/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-regions.md) for the provider-specific parameters and requirements.

