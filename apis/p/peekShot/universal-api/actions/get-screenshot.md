# PeekShot: Get Screenshot

Retrieves a screenshot by request ID from PeekShot.

```
GET https://connect.mindcloud.co/v1/universal/peekShot/latest/actions/get-screenshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PeekShot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peekShot/latest/actions/get-screenshot?connectionId=$CONNECTION_ID&requestId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peekShot/latest/actions/get-screenshot?${params}`, {
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
| `requestId` | number | yes | Unique ID of the screenshot request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": 1,
        "screenshotUrl": "https://example.com",
        "status": "string",
        "url": "https://example.com"
      },
      "message": "string",
      "status": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.id` | number | Screenshot request ID. |
| `data.screenshotUrl` | string | Rendered screenshot URL. |
| `data.status` | string | Screenshot processing status. |
| `data.url` | string | Captured page URL. |
| `message` | string | Provider message. |
| `status` | string | Request status. |
| `statusCode` | number | HTTP-style status code returned by the provider. |

## Native endpoint

Through the native PeekShot API, this operation is `GET /screenshots/:requestId` (base URL `https://api.peekshot.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-screenshot.md) for the provider-specific parameters and requirements.

