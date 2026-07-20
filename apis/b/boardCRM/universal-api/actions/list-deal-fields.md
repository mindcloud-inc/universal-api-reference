# BoardCRM: List Deal Fields

Retrieves custom deal fields from BoardCRM.

```
GET https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/list-deal-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoardCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/list-deal-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/list-deal-fields?${params}`, {
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
      "data": [
        {
          "111547": {
            "alias": "string",
            "entity": "string",
            "fromApi": true,
            "id": 1,
            "isHidden": true,
            "maxLength": 1,
            "protected": true,
            "required": true,
            "sorting": 1,
            "title": "string",
            "type": "string"
          },
          "111548": {
            "alias": "string",
            "entity": "string",
            "fromApi": true,
            "id": 1,
            "isHidden": true,
            "maxLength": 1,
            "protected": true,
            "required": true,
            "sorting": 1,
            "title": "string",
            "type": "string"
          },
          "111549": {
            "alias": "string",
            "entity": "string",
            "fromApi": true,
            "id": 1,
            "isHidden": true,
            "maxLength": 1,
            "protected": true,
            "required": true,
            "sorting": 1,
            "title": "string",
            "type": "string"
          },
          "111563": {
            "alias": "string",
            "entity": "string",
            "fromApi": true,
            "id": 1,
            "isHidden": true,
            "maxLength": 1,
            "protected": true,
            "required": true,
            "sorting": 1,
            "title": "string",
            "type": "string"
          }
        }
      ],
      "meta": {
        "action": {
          "body": {
            "access_token": "string"
          },
          "id": "string",
          "operation": "string",
          "slug": "string"
        },
        "curl": "https://example.com",
        "message": "string",
        "request": {
          "arguments": {
            "body": {
              "access_token": "string"
            }
          },
          "data": {
            "access_token": "string"
          },
          "headers": {
            "Accept": "string"
          },
          "method": "string",
          "originalData": {
            "credentials": {
              "apiKey": "string",
              "id": "string",
              "label": "string",
              "type": "string"
            },
            "data": {
              "access_token": "string"
            },
            "headers": {
              "Authorization": "string",
              "common": {
                "Accept": "string"
              },
              "Content-Type": "string"
            }
          },
          "url": "https://example.com"
        },
        "response": {
          "config": {
            "adapter": [
              "string"
            ],
            "allowAbsoluteUrls": true,
            "baseURL": "https://example.com",
            "data": "string",
            "headers": {
              "Accept": "string",
              "Accept-Encoding": "string",
              "Authorization": "string",
              "Content-Length": "string",
              "Content-Type": "string",
              "User-Agent": "string"
            },
            "maxBodyLength": {},
            "maxContentLength": {},
            "maxRedirects": 1,
            "meta": {
              "body": {
                "access_token": "string"
              }
            },
            "method": "string",
            "timeout": 1,
            "transformRequest": [
              {}
            ],
            "transformResponse": [
              {}
            ],
            "transitional": {
              "clarifyTimeoutError": true,
              "forcedJSONParsing": true,
              "legacyInterceptorReqResOrdering": true,
              "silentJSONParsing": true
            },
            "url": "https://example.com",
            "xsrfCookieName": "Ava Chen",
            "xsrfHeaderName": "Ava Chen"
          },
          "headers": {
            "access-control-allow-credentials": "string",
            "access-control-expose-headers": "string",
            "cache-control": "string",
            "connection": "string",
            "content-security-policy": "string",
            "content-type": "string",
            "date": "string",
            "expires": "string",
            "pragma": "string",
            "server": "string",
            "set-cookie": "string",
            "transfer-encoding": "string",
            "x-powered-by": "string"
          },
          "request": {
            "_closed": true,
            "_contentLength": "string",
            "_defaultKeepAlive": true,
            "_ended": true,
            "_eventsCount": 1,
            "_hasBody": true,
            "_header": "string",
            "_headerSent": true,
            "_keepAliveTimeout": 1,
            "_last": true,
            "_removedConnection": true,
            "_removedContLen": true,
            "_removedTE": true,
            "_trailer": "string",
            "aborted": true,
            "chunkedEncoding": true,
            "destroyed": true,
            "finished": true,
            "host": "string",
            "maxHeadersCount": {},
            "maxRequestsOnConnectionReached": true,
            "method": "string",
            "outputSize": 1,
            "parser": {},
            "path": "string",
            "protocol": "string",
            "reusedSocket": true,
            "sendDate": true,
            "shouldKeepAlive": true,
            "strictContentLength": true,
            "timeoutCb": {},
            "upgradeOrConnect": true,
            "useChunkedEncodingByDefault": true,
            "writable": true
          },
          "status": 1,
          "statusText": "string"
        }
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].111547.alias` | string |  |
| `data[].111547.entity` | string |  |
| `data[].111547.fromApi` | boolean |  |
| `data[].111547.id` | number |  |
| `data[].111547.isHidden` | boolean |  |
| `data[].111547.maxLength` | number |  |
| `data[].111547.protected` | boolean |  |
| `data[].111547.required` | boolean |  |
| `data[].111547.sorting` | number |  |
| `data[].111547.title` | string |  |
| `data[].111547.type` | string |  |
| `data[].111548.alias` | string |  |
| `data[].111548.entity` | string |  |
| `data[].111548.fromApi` | boolean |  |
| `data[].111548.id` | number |  |
| `data[].111548.isHidden` | boolean |  |
| `data[].111548.maxLength` | number |  |
| `data[].111548.protected` | boolean |  |
| `data[].111548.required` | boolean |  |
| `data[].111548.sorting` | number |  |
| `data[].111548.title` | string |  |
| `data[].111548.type` | string |  |
| `data[].111549.alias` | string |  |
| `data[].111549.entity` | string |  |
| `data[].111549.fromApi` | boolean |  |
| `data[].111549.id` | number |  |
| `data[].111549.isHidden` | boolean |  |
| `data[].111549.maxLength` | number |  |
| `data[].111549.protected` | boolean |  |
| `data[].111549.required` | boolean |  |
| `data[].111549.sorting` | number |  |
| `data[].111549.title` | string |  |
| `data[].111549.type` | string |  |
| `data[].111563.alias` | string |  |
| `data[].111563.entity` | string |  |
| `data[].111563.fromApi` | boolean |  |
| `data[].111563.id` | number |  |
| `data[].111563.isHidden` | boolean |  |
| `data[].111563.maxLength` | number |  |
| `data[].111563.protected` | boolean |  |
| `data[].111563.required` | boolean |  |
| `data[].111563.sorting` | number |  |
| `data[].111563.title` | string |  |
| `data[].111563.type` | string |  |
| `meta.action.body.access_token` | string |  |
| `meta.action.id` | string |  |
| `meta.action.operation` | string |  |
| `meta.action.slug` | string |  |
| `meta.curl` | string |  |
| `meta.message` | string |  |
| `meta.request.arguments.body.access_token` | string |  |
| `meta.request.data.access_token` | string |  |
| `meta.request.headers.Accept` | string |  |
| `meta.request.method` | string |  |
| `meta.request.originalData.credentials.apiKey` | string |  |
| `meta.request.originalData.credentials.id` | string |  |
| `meta.request.originalData.credentials.label` | string |  |
| `meta.request.originalData.credentials.type` | string |  |
| `meta.request.originalData.data.access_token` | string |  |
| `meta.request.originalData.headers.Authorization` | string |  |
| `meta.request.originalData.headers.common.Accept` | string |  |
| `meta.request.originalData.headers.Content-Type` | string |  |
| `meta.request.url` | string |  |
| `meta.response.config.adapter[]` | string |  |
| `meta.response.config.allowAbsoluteUrls` | boolean |  |
| `meta.response.config.baseURL` | string |  |
| `meta.response.config.data` | string |  |
| `meta.response.config.headers.Accept` | string |  |
| `meta.response.config.headers.Accept-Encoding` | string |  |
| `meta.response.config.headers.Authorization` | string |  |
| `meta.response.config.headers.Content-Length` | string |  |
| `meta.response.config.headers.Content-Type` | string |  |
| `meta.response.config.headers.User-Agent` | string |  |
| `meta.response.config.maxBodyLength` | object |  |
| `meta.response.config.maxContentLength` | object |  |
| `meta.response.config.maxRedirects` | number |  |
| `meta.response.config.meta.body.access_token` | string |  |
| `meta.response.config.method` | string |  |
| `meta.response.config.timeout` | number |  |
| `meta.response.config.transformRequest[]` | object |  |
| `meta.response.config.transformResponse[]` | object |  |
| `meta.response.config.transitional.clarifyTimeoutError` | boolean |  |
| `meta.response.config.transitional.forcedJSONParsing` | boolean |  |
| `meta.response.config.transitional.legacyInterceptorReqResOrdering` | boolean |  |
| `meta.response.config.transitional.silentJSONParsing` | boolean |  |
| `meta.response.config.url` | string |  |
| `meta.response.config.xsrfCookieName` | string |  |
| `meta.response.config.xsrfHeaderName` | string |  |
| `meta.response.headers.access-control-allow-credentials` | string |  |
| `meta.response.headers.access-control-expose-headers` | string |  |
| `meta.response.headers.cache-control` | string |  |
| `meta.response.headers.connection` | string |  |
| `meta.response.headers.content-security-policy` | string |  |
| `meta.response.headers.content-type` | string |  |
| `meta.response.headers.date` | string |  |
| `meta.response.headers.expires` | string |  |
| `meta.response.headers.pragma` | string |  |
| `meta.response.headers.server` | string |  |
| `meta.response.headers.set-cookie` | string |  |
| `meta.response.headers.transfer-encoding` | string |  |
| `meta.response.headers.x-powered-by` | string |  |
| `meta.response.request._closed` | boolean |  |
| `meta.response.request._contentLength` | string |  |
| `meta.response.request._defaultKeepAlive` | boolean |  |
| `meta.response.request._ended` | boolean |  |
| `meta.response.request._eventsCount` | number |  |
| `meta.response.request._hasBody` | boolean |  |
| `meta.response.request._header` | string |  |
| `meta.response.request._headerSent` | boolean |  |
| `meta.response.request._keepAliveTimeout` | number |  |
| `meta.response.request._last` | boolean |  |
| `meta.response.request._removedConnection` | boolean |  |
| `meta.response.request._removedContLen` | boolean |  |
| `meta.response.request._removedTE` | boolean |  |
| `meta.response.request._trailer` | string |  |
| `meta.response.request.aborted` | boolean |  |
| `meta.response.request.chunkedEncoding` | boolean |  |
| `meta.response.request.destroyed` | boolean |  |
| `meta.response.request.finished` | boolean |  |
| `meta.response.request.host` | string |  |
| `meta.response.request.maxHeadersCount` | object |  |
| `meta.response.request.maxRequestsOnConnectionReached` | boolean |  |
| `meta.response.request.method` | string |  |
| `meta.response.request.outputSize` | number |  |
| `meta.response.request.parser` | object |  |
| `meta.response.request.path` | string |  |
| `meta.response.request.protocol` | string |  |
| `meta.response.request.reusedSocket` | boolean |  |
| `meta.response.request.sendDate` | boolean |  |
| `meta.response.request.shouldKeepAlive` | boolean |  |
| `meta.response.request.strictContentLength` | boolean |  |
| `meta.response.request.timeoutCb` | object |  |
| `meta.response.request.upgradeOrConnect` | boolean |  |
| `meta.response.request.useChunkedEncodingByDefault` | boolean |  |
| `meta.response.request.writable` | boolean |  |
| `meta.response.status` | number |  |
| `meta.response.statusText` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native BoardCRM API, this operation is `POST /field/list` (base URL `https://api.boardcrm.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deal-fields.md) for the provider-specific parameters and requirements.

