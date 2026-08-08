# HTTP: Send HTTP Request

Sends an HTTP request to any URL.

```
GET https://connect.mindcloud.co/v1/universal/httpRequest/latest/actions/send-http-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HTTP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/httpRequest/latest/actions/send-http-request?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com%2Fpath%3Fquery%3Dvalue&method=DELETE" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com/path?query=value",
  "method": "DELETE"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/httpRequest/latest/actions/send-http-request?${params}`, {
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
| `url` | string | yes | Full URL to request, including any query string. Signed links are passed through unchanged. Example: `https://example.com/path?query=value`. |
| `method` | list<string> | yes | HTTP method to use. One of: `DELETE`, `GET`, `HEAD`, `OPTIONS`, `PATCH`, `POST`, `PUT`. |
| `headers` | array<object> | no | HTTP headers to send, as an array of { key, value } pairs. |
| `bodyFormat` | list<string> | no | Request body encoding. Leave unset (None) for requests without a body. One of: `Form Data`, `JSON`, `None`, `Raw`, `x-www-form-urlencoded`. |
| `bodyJson` | object | no | JSON request body, sent as provided. Used when Body Format is JSON. |
| `headers[].key` | string | no |  |
| `headers[].value` | string | no |  |
| `queryParams[].key` | string | no |  |
| `queryParams[].value` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `queryParams` | array<object> | no | Extra query parameters as { key, value } pairs. Parameters already in the URL are kept. |
| `bodyRaw` | string | no | Raw text request body. Used when Body Format is Raw. |
| `bodyFormData` | object | no | Multipart form fields as key-value pairs. Used when Body Format is Form Data. |
| `bodyXWwwForm` | object | no | URL-encoded form fields as key-value pairs. Used when Body Format is x-www-form-urlencoded. |
| `contentType` | string | no | Content-Type header for Raw bodies, e.g. text/csv. |
| `followRedirects` | boolean | no | Follow HTTP redirects (up to 10). Defaults to true. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HTTP API returns.

## Native endpoint

Through the native HTTP API, this operation is `GET :url`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-http-request.md) for the provider-specific parameters and requirements.

