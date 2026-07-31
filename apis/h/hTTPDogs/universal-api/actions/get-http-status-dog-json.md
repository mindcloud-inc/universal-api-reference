# HTTP Dogs: Get HTTP Status Dog JSON



```
GET https://connect.mindcloud.co/v1/universal/hTTPDogs/latest/actions/get-http-status-dog-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HTTP Dogs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hTTPDogs/latest/actions/get-http-status-dog-json?connectionId=$CONNECTION_ID&statusCode=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "statusCode": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hTTPDogs/latest/actions/get-http-status-dog-json?${params}`, {
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
| `statusCode` | number | yes | Required three-digit HTTP response status code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "image": "string",
      "status_code": 1,
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `image` | string | Dog image URL. |
| `status_code` | number | HTTP status code. |
| `title` | string | Status title. |
| `url` | string | Status documentation URL. |

## Native endpoint

Through the native HTTP Dogs API, this operation is `GET /:statusCode.json` (base URL `https://http.dog`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-http-status-dog-json.md) for the provider-specific parameters and requirements.

