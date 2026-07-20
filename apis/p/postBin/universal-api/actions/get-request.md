# PostBin: Get Request

Retrieves a stored request from a PostBin bin.

```
GET https://connect.mindcloud.co/v1/universal/postBin/latest/actions/get-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostBin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postBin/latest/actions/get-request?connectionId=$CONNECTION_ID&binId=string&reqId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "binId": "string",
  "reqId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postBin/latest/actions/get-request?${params}`, {
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
| `binId` | string | yes | The PostBin bin identifier. |
| `reqId` | string | yes | The request identifier returned by the capture endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "binId": "string",
      "body": {},
      "headers": {},
      "inserted": 1,
      "ip": "string",
      "method": "string",
      "path": "string",
      "query": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `binId` | string | Bin identifier that received the request. |
| `body` | object | Captured request body. |
| `headers` | object | Captured request headers. |
| `inserted` | number | UTC timestamp in milliseconds when the request was stored. |
| `ip` | string | Observed client IP address. |
| `method` | string | HTTP method used for the captured request. |
| `path` | string | Captured request path. |
| `query` | object | Captured query parameters. |

## Native endpoint

Through the native PostBin API, this operation is `GET /bin/:binId/req/:reqId` (base URL `https://www.postb.in/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-request.md) for the provider-specific parameters and requirements.

