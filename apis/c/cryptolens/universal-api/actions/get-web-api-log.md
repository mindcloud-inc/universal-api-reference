# Cryptolens: Get Web API Log

Retrieves Web API logs from Cryptolens.

```
GET https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-web-api-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptolens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-web-api-log?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-web-api-log?${params}`, {
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
| `productId` | number | no | Product ID to filter on. |
| `key` | string | no | License key string to filter on. |
| `machineCode` | string | no | Machine code to filter on. |
| `friendlyName` | string | no | Friendly name filter. |
| `states` | string | no | JSON list of integer state codes to filter on. |
| `time` | string | no | JSON interval filter for request time. |
| `limit` | number | no | Maximum number of logs to return. |
| `startingAfter` | string | no | Cursor for logs after the given id. |
| `endingBefore` | string | no | Cursor for logs before the given id. |
| `orderBy` | string | no | Ordering value such as Id descending. |
| `anomalyClassification` | boolean | no | Whether to include anomaly classification details. |
| `v` | string | no | Method version. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "logs": [
        {}
      ],
      "message": "string",
      "result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `logs` | array<object> | List of web API log entries returned by Get Web API Log. |
| `message` | string | Message returned by Get Web API Log. |
| `result` | number | Result code returned by Get Web API Log. |

## Native endpoint

Through the native Cryptolens API, this operation is `GET /api/ai/GetWebAPILog` (base URL `https://api.cryptolens.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-web-api-log.md) for the provider-specific parameters and requirements.

