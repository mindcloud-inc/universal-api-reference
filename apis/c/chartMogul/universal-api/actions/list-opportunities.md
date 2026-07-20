# ChartMogul: List Opportunities

Retrieves opportunities from ChartMogul.

```
GET https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-opportunities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChartMogul `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-opportunities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-opportunities?${params}`, {
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
      "amountInCents": 1,
      "currency": "string",
      "customerUuid": "string",
      "estimatedCloseDate": "2026-05-07T12:00:00.000Z",
      "forecastCategory": "string",
      "owner": "string",
      "pipeline": "string",
      "pipelineStage": "string",
      "type": "string",
      "uuid": "string",
      "winLikelihood": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountInCents` | number |  |
| `currency` | string |  |
| `customerUuid` | string |  |
| `estimatedCloseDate` | date |  |
| `forecastCategory` | string |  |
| `owner` | string |  |
| `pipeline` | string |  |
| `pipelineStage` | string |  |
| `type` | string |  |
| `uuid` | string |  |
| `winLikelihood` | number |  |

## Native endpoint

Through the native ChartMogul API, this operation is `GET /opportunities` (base URL `https://api.chartmogul.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-opportunities.md) for the provider-specific parameters and requirements.

