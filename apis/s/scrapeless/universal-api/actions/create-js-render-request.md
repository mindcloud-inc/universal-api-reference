# Scrapeless: Create JS Render Request

Creates a JS render request in Scrapeless.

```
POST https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/create-js-render-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/create-js-render-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "proxy": {},
  "proxy.country": "string",
  "input": {},
  "input.url": "https://example.com",
  "input.cookies[].domain": "string",
  "input.cookies[].path": "string",
  "input.cookies[].name": "Ava Chen",
  "input.cookies[].value": "string",
  "input.jsRender": {},
  "input.jsRender.enabled": true,
  "input.jsRender.response": {},
  "input.jsRender.response.type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/create-js-render-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "proxy": {},
    "proxy.country": "string",
    "input": {},
    "input.url": "https://example.com",
    "input.cookies[].domain": "string",
    "input.cookies[].path": "string",
    "input.cookies[].name": "Ava Chen",
    "input.cookies[].value": "string",
    "input.jsRender": {},
    "input.jsRender.enabled": true,
    "input.jsRender.response": {},
    "input.jsRender.response.type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `proxy` | object | yes | proxy info |
| `proxy.country` | string | yes | proxy country, see more in [Scrapeless proxy documentation](https://docs.scrapeless.com/en/proxies/features/proxy/) |
| `proxy.url` | string | no | proxy url |
| `input` | object | yes |  |
| `input.url` | string | yes | target URL |
| `input.cookies[]` | array<object> | no | cookies for JS render |
| `input.cookies[].domain` | string | yes | cookie domain |
| `input.cookies[].path` | string | yes | cookie path |
| `input.cookies[].name` | string | yes | cookie name |
| `input.cookies[].value` | string | yes | cookie value |
| `input.cookies[].expires` | number | no | cookie expiration date as the number of seconds since the UNIX epoch. Set to `-1` for session cookies |
| `input.cookies[].sameSite` | string | no | cookie SameSite type |
| `input.cookies[].secure` | boolean | no | `true` if cookie is secure |
| `input.jsRender` | object | yes | JS render options |
| `input.jsRender.enabled` | boolean | yes | enable JS rendering |
| `input.jsRender.headless` | boolean | no | whether processing in headless mode |
| `input.jsRender.waitUntil` | string | no | when to consider waiting succeeds. given an array of event strings, waiting is considered to be successful after all events have been fired |
| `input.jsRender.instructions[]` | array<object> | no | [JavaScript Instructions Reference](https://docs.scrapeless.com/en/web-unlocker/features/js-render/#javascript-instructions-reference) |
| `input.jsRender.instructions[].wait` | number | no | Wait for Wait for element |
| `input.jsRender.instructions[].waitFor` | object | no | Wait for element |
| `input.jsRender.instructions[].waitFor.0` | string | no | Selector |
| `input.jsRender.instructions[].waitFor.1` | number | no | Timeout(s) |
| `input.jsRender.instructions[].click[]` | array<object> | no | Click element |
| `input.jsRender.instructions[].click[].0` | string | no | Selector |
| `input.jsRender.instructions[].click[].1` | number | no | Timeout(s) |
| `input.jsRender.instructions[].fill` | object | no | Fill form |
| `input.jsRender.instructions[].fill.0` | string | no | Selector |
| `input.jsRender.instructions[].fill.1` | string | no | value |
| `input.jsRender.instructions[].keyboard` | object | no | [Keyboard Operations](https://docs.scrapeless.com/en/web-unlocker/features/js-render/#keyboard-operations) |
| `input.jsRender.instructions[].keyboard.0` | string | no | Press a specific [keyInput](https://pptr.dev/api/puppeteer.keyinput) |
| `input.jsRender.instructions[].keyboard.1` | string | no | key ｜ value |
| `input.jsRender.instructions[].keyboard.2` | number | no | delay(ms) |
| `input.jsRender.instructions[].evaluate` | string | no | Execute custom javascript code |
| `input.jsRender.block` | object | no | resources or urls to block |
| `input.jsRender.block.resources[]` | array<string> | no | block resources |
| `input.jsRender.block.urls[]` | array<string> | no | block urls |
| `input.jsRender.response` | object | yes | response config |
| `input.jsRender.response.type` | string | yes | response type |
| `input.jsRender.response.options` | object | no | response options |
| `input.jsRender.response.options.selector` | string | no | CSS selector for output filters and specified response type. only works when type equals to one of`html \| plaintext \| markdown \| png \| jpeg` |
| `input.jsRender.response.options.fullPage` | boolean | no | whether takes a screen of the full page. only works when type equals to`png`or`jpeg` |
| `input.jsRender.response.options.urls[]` | array<string> | no | only include requests whose URL matches any of specified strings or patterns, supports substring match. only works when type equals to`network` |
| `input.jsRender.response.options.status[]` | array<string> | no | only include requests with specified HTTP status codes. only works when type equals to`network` |
| `input.jsRender.response.options.methods[]` | array<string> | no | only include requests with specified HTTP methods (e.g., GET, POST). only works when type equals to`network` |
| `input.jsRender.response.options.outputs` | string | no | filter data from HTML, it accepts a comma-separated list of filter names and returns the results in a escaped JSON string format. only works when type equals to`content` |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | string |  |

## Native endpoint

Through the native Scrapeless API, this operation is `POST /api/v2/unlocker/request` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-js-render-request.md) for the provider-specific parameters and requirements.

