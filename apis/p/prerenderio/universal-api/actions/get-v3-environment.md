# Prerender.io: List Environment

Retrieves environment settings from Prerender.io.

```
GET https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-environment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

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



## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiToken` | string |  |
| `automaticRecachingPaused` | boolean |  |
| `cacheFreshness` | number |  |
| `customRecacheDelay` | number |  |
| `desktopUserAgent` | string |  |
| `desktopViewport` | string |  |
| `enableServiceWorker` | boolean |  |
| `enforceHttpsProtocol` | boolean |  |
| `environmentName` | string |  |
| `extractHiddenCss` | boolean |  |
| `fixHeadTag` | boolean |  |
| `ignoreAllQueryParams` | boolean |  |
| `imageLoading` | boolean |  |
| `minimumBodyLength` | number |  |
| `mobileOptimizedRendering` | boolean |  |
| `mobileUserAgent` | string |  |
| `mobileViewport` | string |  |
| `onlyServeCacheHits` | boolean |  |
| `parseShadowDom` | boolean |  |
| `preCheckStatus` | boolean |  |
| `prerenderCssLocation` | string |  |
| `queryParamsWhitelist` | boolean |  |
| `removeStyleTags` | boolean |  |
| `removeUrlHash` | boolean |  |
| `renderingTimeout` | number |  |
| `renderLocation` | string |  |
| `retryDirtyRenders` | boolean |  |
| `retryTimedOutRenders` | boolean |  |
| `scrollEnabled` | boolean |  |
| `scrollToBottomAfterPageLoad` | boolean |  |
| `skipCustomElementsForcePolyfill` | boolean |  |

## Native endpoint

Through the native Prerender.io API, this operation is `GET /v3/environment` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-v3-environment.md) for the provider-specific parameters and requirements.

