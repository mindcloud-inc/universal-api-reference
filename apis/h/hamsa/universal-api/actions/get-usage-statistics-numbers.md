# Hamsa: Get Usage Statistics Numbers

Retrieves usage statistic totals from Hamsa.

```
GET https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-usage-statistics-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hamsa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-usage-statistics-numbers?connectionId=$CONNECTION_ID&startPeriod=string&endPeriod=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startPeriod": "string",
  "endPeriod": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-usage-statistics-numbers?${params}`, {
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
      "price": {
        "unit": "string",
        "value": 1
      },
      "requests": {
        "unit": "string",
        "value": "string"
      },
      "tokens": {
        "unit": "string",
        "value": 1
      },
      "transcription": {
        "unit": "string",
        "value": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `price.unit` | string |  |
| `price.value` | number |  |
| `requests.unit` | string |  |
| `requests.value` | string |  |
| `tokens.unit` | string |  |
| `tokens.value` | number |  |
| `transcription.unit` | string |  |
| `transcription.value` | number |  |

## Native endpoint

Through the native Hamsa API, this operation is `GET /v1/projects/statistics/numbers` (base URL `https://api.tryhamsa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage-statistics-numbers.md) for the provider-specific parameters and requirements.

