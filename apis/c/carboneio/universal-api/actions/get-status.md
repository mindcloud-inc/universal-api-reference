# Carbone.io: Get Status

Retrieves service status from Carbone.io.

```
GET https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/get-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Carbone.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/get-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/get-status?${params}`, {
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
      "code": 1,
      "message": "string",
      "success": true,
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | HTTP-style status code from Carbone. |
| `message` | string | Provider status message. |
| `success` | boolean | Whether the API is healthy. |
| `version` | string | Reported Carbone API version. |

## Native endpoint

Through the native Carbone.io API, this operation is `GET /status` (base URL `https://api.carbone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-status.md) for the provider-specific parameters and requirements.

