# Reamaze: Get Response Time Report



```
GET https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/get-response-time-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reamaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/get-response-time-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/get-response-time-report?${params}`, {
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
| `startDate` | date | no | The `start_date` value can used to choose the start of the report. |
| `endDate` | date | no | The `end_date` value can used to choose the end of the report. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endDate": "string",
      "responseTimes": {},
      "startDate": "string",
      "summary": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endDate` | string |  |
| `responseTimes` | object |  |
| `startDate` | string |  |
| `summary` | object |  |

## Native endpoint

Through the native Reamaze API, this operation is `GET /reports/response_time` (base URL `https://{{credentials.brand}}.reamaze.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-response-time-report.md) for the provider-specific parameters and requirements.

