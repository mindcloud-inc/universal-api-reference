# HasData: Search Google Trends

Retrieves Google Trends results from HasData.

```
GET https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-google-trends
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HasData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-google-trends?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-google-trends?${params}`, {
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
| `dataType` | string | no | Trend data type, such as timeseries or geoMap. |
| `date` | string | no | Date range or shortcut such as today 12-m. |
| `geo` | string | no | Geographic region code for Google Trends. |
| `q` | string | yes | Search term for Google Trends. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "interestOverTime": {
        "timelineData": [
          {}
        ]
      },
      "requestMetadata": {
        "id": "string",
        "json": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `interestOverTime.timelineData` | array<object> | Timeline data points for interest over time. |
| `requestMetadata.id` | string | HasData request identifier. |
| `requestMetadata.json` | string | URL to the JSON payload file. |
| `requestMetadata.status` | string | Request status returned by HasData. |

## Native endpoint

Through the native HasData API, this operation is `GET /scrape/google-trends/search` (base URL `https://api.hasdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-trends.md) for the provider-specific parameters and requirements.

