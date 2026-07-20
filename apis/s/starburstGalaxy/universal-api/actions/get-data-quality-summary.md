# Starburst Galaxy: Get data quality summary



```
GET https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/get-data-quality-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starburst Galaxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/get-data-quality-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/get-data-quality-summary?${params}`, {
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
      "catalogSummaries": [
        {}
      ],
      "categoryCounts": [
        {}
      ],
      "dailySummaries": [
        {}
      ],
      "severityCounts": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `catalogSummaries` | array<object> |  |
| `categoryCounts` | array<object> |  |
| `dailySummaries` | array<object> |  |
| `severityCounts` | array<object> |  |

## Native endpoint

Through the native Starburst Galaxy API, this operation is `GET /public/api/v1/dataQualitySummary` (base URL `https://mindcloud.galaxy.starburst.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-quality-summary.md) for the provider-specific parameters and requirements.

