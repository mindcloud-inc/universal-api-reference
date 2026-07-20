# Prerender.io Universal API Examples

These examples use the MindCloud API key and Prerender.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Environment

Retrieves environment settings from Prerender.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-environment?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-environment?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "apiToken": "string",
      "automaticRecachingPaused": true,
      "cacheFreshness": 1,
      "customRecacheDelay": 1,
      "desktopUserAgent": "string",
      "desktopViewport": "string",
      "enableServiceWorker": true,
      "enforceHttpsProtocol": true,
      "environmentName": "Ava Chen",
      "extractHiddenCss": true,
      "fixHeadTag": true,
      "ignoreAllQueryParams": true,
      "imageLoading": true,
      "minimumBodyLength": 1,
      "mobileOptimizedRendering": true,
      "mobileUserAgent": "string",
      "mobileViewport": "string",
      "onlyServeCacheHits": true,
      "parseShadowDom": true,
      "preCheckStatus": true,
      "prerenderCssLocation": "string",
      "queryParamsWhitelist": true,
      "removeStyleTags": true,
      "removeUrlHash": true,
      "renderingTimeout": 1,
      "renderLocation": "string",
      "retryDirtyRenders": true,
      "retryTimedOutRenders": true,
      "scrollEnabled": true,
      "scrollToBottomAfterPageLoad": true,
      "skipCustomElementsForcePolyfill": true
    }
  ],
  "meta": {}
}
```

See the full [List Environment action reference](actions/get-v3-environment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/prerenderio/latest/actions/get-v3-environment).

## Update Domain 404 Check Toggle All

Updates all domain 404 checks in Prerender.io.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/patch-v3-domain-404-check-toggle-all-enabled" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "enabled": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/patch-v3-domain-404-check-toggle-all-enabled', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "enabled": true
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Update Domain 404 Check Toggle All action reference](actions/patch-v3-domain-404-check-toggle-all-enabled.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/prerenderio/latest/actions/patch-v3-domain-404-check-toggle-all-enabled).
