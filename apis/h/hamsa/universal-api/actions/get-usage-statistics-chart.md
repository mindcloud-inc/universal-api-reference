# Hamsa: Get Usage Statistics Chart

Retrieves usage statistics chart data from Hamsa.

```
GET https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-usage-statistics-chart
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hamsa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-usage-statistics-chart?connectionId=$CONNECTION_ID&startPeriod=string&endPeriod=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startPeriod": "string",
  "endPeriod": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-usage-statistics-chart?${params}`, {
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
| `startPeriod` | string | yes |  |
| `endPeriod` | string | yes |  |
| `projectId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cost": [
        {
          "date": "2026-05-07T12:00:00.000Z",
          "unit": "string",
          "value": 1
        }
      ],
      "requests": [
        {
          "date": "2026-05-07T12:00:00.000Z",
          "unit": "string",
          "value": 1
        }
      ],
      "tokens": [
        {
          "date": "2026-05-07T12:00:00.000Z",
          "unit": "string",
          "value": 1
        }
      ],
      "transcription": [
        {
          "date": "2026-05-07T12:00:00.000Z",
          "unit": "string",
          "value": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cost[].date` | date |  |
| `cost[].unit` | string |  |
| `cost[].value` | number |  |
| `requests[].date` | date |  |
| `requests[].unit` | string |  |
| `requests[].value` | number |  |
| `tokens[].date` | date |  |
| `tokens[].unit` | string |  |
| `tokens[].value` | number |  |
| `transcription[].date` | date |  |
| `transcription[].unit` | string |  |
| `transcription[].value` | number |  |

## Native endpoint

Through the native Hamsa API, this operation is `GET /v1/projects/statistics/chart` (base URL `https://api.tryhamsa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage-statistics-chart.md) for the provider-specific parameters and requirements.

