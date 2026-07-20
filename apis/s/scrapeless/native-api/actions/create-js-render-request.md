# Create JS Render Request with Scrapeless

Creates a JS render request in Scrapeless.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/unlocker/request`
- **Base URL:** `https://api.scrapeless.com`
- **Official documentation:** [Create JS Render Request](https://apidocs.scrapeless.com/api-12948840)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `proxy` | body | `object` | yes | proxy info |
| `proxy.country` | body | `string` | yes | proxy country, see more in [Scrapeless proxy documentation](https://docs.scrapeless.com/en/proxies/features/proxy/) |
| `proxy.url` | body | `string` | no | proxy url |
| `input` | body | `object` | yes | — |
| `input.url` | body | `string` | yes | target URL |
| `input.cookies[]` | body | `array<object>` | no | cookies for JS render |
| `input.cookies[].domain` | body | `string` | yes | cookie domain |
| `input.cookies[].path` | body | `string` | yes | cookie path |
| `input.cookies[].name` | body | `string` | yes | cookie name |
| `input.cookies[].value` | body | `string` | yes | cookie value |
| `input.cookies[].expires` | body | `number` | no | cookie expiration date as the number of seconds since the UNIX epoch. Set to `-1` for session cookies |
| `input.cookies[].sameSite` | body | `string` | no | cookie SameSite type |
| `input.cookies[].secure` | body | `boolean` | no | `true` if cookie is secure |
| `input.jsRender` | body | `object` | yes | JS render options |
| `input.jsRender.enabled` | body | `boolean` | yes | enable JS rendering |
| `input.jsRender.headless` | body | `boolean` | no | whether processing in headless mode |
| `input.jsRender.waitUntil` | body | `string` | no | when to consider waiting succeeds. given an array of event strings, waiting is considered to be successful after all events have been fired |
| `input.jsRender.instructions[]` | body | `array<object>` | no | [JavaScript Instructions Reference](https://docs.scrapeless.com/en/web-unlocker/features/js-render/#javascript-instructions-reference) |
| `input.jsRender.instructions[].wait` | body | `number` | no | Wait for Wait for element |
| `input.jsRender.instructions[].waitFor` | body | `object` | no | Wait for element |
| `input.jsRender.instructions[].waitFor.0` | body | `string` | no | Selector |
| `input.jsRender.instructions[].waitFor.1` | body | `number` | no | Timeout(s) |
| `input.jsRender.instructions[].click[]` | body | `array<object>` | no | Click element |
| `input.jsRender.instructions[].click[].0` | body | `string` | no | Selector |
| `input.jsRender.instructions[].click[].1` | body | `number` | no | Timeout(s) |
| `input.jsRender.instructions[].fill` | body | `object` | no | Fill form |
| `input.jsRender.instructions[].fill.0` | body | `string` | no | Selector |
| `input.jsRender.instructions[].fill.1` | body | `string` | no | value |
| `input.jsRender.instructions[].keyboard` | body | `object` | no | [Keyboard Operations](https://docs.scrapeless.com/en/web-unlocker/features/js-render/#keyboard-operations) |
| `input.jsRender.instructions[].keyboard.0` | body | `string` | no | Press a specific [keyInput](https://pptr.dev/api/puppeteer.keyinput) |
| `input.jsRender.instructions[].keyboard.1` | body | `string` | no | key ｜ value |
| `input.jsRender.instructions[].keyboard.2` | body | `number` | no | delay(ms) |
| `input.jsRender.instructions[].evaluate` | body | `string` | no | Execute custom javascript code |
| `input.jsRender.block` | body | `object` | no | resources or urls to block |
| `input.jsRender.block.resources[]` | body | `array<string>` | no | block resources |
| `input.jsRender.block.urls[]` | body | `array<string>` | no | block urls |
| `input.jsRender.response` | body | `object` | yes | response config |
| `input.jsRender.response.type` | body | `string` | yes | response type |
| `input.jsRender.response.options` | body | `object` | no | response options |
| `input.jsRender.response.options.selector` | body | `string` | no | CSS selector for output filters and specified response type. only works when type equals to one of`html \| plaintext \| markdown \| png \| jpeg` |
| `input.jsRender.response.options.fullPage` | body | `boolean` | no | whether takes a screen of the full page.  only works when type equals to`png`or`jpeg` |
| `input.jsRender.response.options.urls[]` | body | `array<string>` | no | only include requests whose URL matches any of specified strings or patterns, supports substring match. only works when type equals to`network` |
| `input.jsRender.response.options.status[]` | body | `array<string>` | no | only include requests with specified HTTP status codes. only works when type equals to`network` |
| `input.jsRender.response.options.methods[]` | body | `array<string>` | no | only include requests with specified HTTP methods (e.g., GET, POST). only works when type equals to`network` |
| `input.jsRender.response.options.outputs` | body | `string` | no | filter data from HTML, it accepts a comma-separated list of filter names and returns the results in a escaped JSON string format. only works when type equals to`content` |
