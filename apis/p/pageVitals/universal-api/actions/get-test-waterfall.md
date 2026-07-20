# PageVitals: Get Test Waterfall



```
GET https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/get-test-waterfall
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PageVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/get-test-waterfall?connectionId=$CONNECTION_ID&websiteId=string&testId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "testId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/get-test-waterfall?${params}`, {
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
| `websiteId` | string | yes |  |
| `testId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blocked": 1,
      "connect": 1,
      "dns": 1,
      "http": "string",
      "index": 1,
      "longTasks": [
        {}
      ],
      "method": "string",
      "opportunities": {},
      "priority": "string",
      "receive": 1,
      "renderBlocking": true,
      "send": 1,
      "size": 1,
      "start": 1,
      "status": 1,
      "time": 1,
      "tls": 1,
      "type": "string",
      "uncompressedSize": 1,
      "url": "https://example.com",
      "wait": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocked` | number |  |
| `connect` | number |  |
| `dns` | number |  |
| `http` | string |  |
| `index` | number |  |
| `longTasks` | array<object> |  |
| `method` | string |  |
| `opportunities` | object |  |
| `priority` | string |  |
| `receive` | number |  |
| `renderBlocking` | boolean |  |
| `send` | number |  |
| `size` | number |  |
| `start` | number |  |
| `status` | number |  |
| `time` | number |  |
| `tls` | number |  |
| `type` | string |  |
| `uncompressedSize` | number |  |
| `url` | string |  |
| `wait` | number |  |

## Native endpoint

Through the native PageVitals API, this operation is `GET /:websiteId/tests/:testId/waterfall` (base URL `https://api.pagevitals.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-test-waterfall.md) for the provider-specific parameters and requirements.

