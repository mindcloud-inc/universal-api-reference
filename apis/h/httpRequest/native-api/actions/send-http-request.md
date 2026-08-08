# Send HTTP Request with HTTP

Sends an HTTP request to any URL.

## Endpoint

- **Method:** `GET`
- **URL:** `:url`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | path | `string` | yes | Full URL to request, including any query string. Signed links are passed through unchanged. |
| `method` | body | `list<string>` | yes | HTTP method to use. Accepted values: `DELETE`, `GET`, `HEAD`, `OPTIONS`, `PATCH`, `POST`, `PUT`. |
| `headers` | body | `array<object>` | no | HTTP headers to send, as an array of { key, value } pairs. |
| `queryParams` | body | `array<object>` | no | Extra query parameters as { key, value } pairs. Parameters already in the URL are kept. |
| `bodyFormat` | body | `list<string>` | no | Request body encoding. Leave unset (None) for requests without a body. Accepted values: `Form Data`, `JSON`, `None`, `Raw`, `x-www-form-urlencoded`. |
| `bodyJson` | body | `object` | no | JSON request body, sent as provided. Used when Body Format is JSON. |
| `bodyRaw` | body | `string` | no | Raw text request body. Used when Body Format is Raw. |
| `bodyFormData` | body | `object` | no | Multipart form fields as key-value pairs. Used when Body Format is Form Data. |
| `bodyXWwwForm` | body | `object` | no | URL-encoded form fields as key-value pairs. Used when Body Format is x-www-form-urlencoded. |
| `contentType` | body | `string` | no | Content-Type header for Raw bodies, e.g. text/csv. |
| `followRedirects` | body | `boolean` | no | Follow HTTP redirects (up to 10). Defaults to true. |
| `headers[].key` | body | `string` | no | — |
| `headers[].value` | body | `string` | no | — |
| `queryParams[].key` | body | `string` | no | — |
| `queryParams[].value` | body | `string` | no | — |
