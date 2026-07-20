# BoardCRM Universal API Examples

These examples use the MindCloud API key and BoardCRM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Deal Fields

Retrieves custom deal fields from BoardCRM.

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

Example response:

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

See the full [List Deal Fields action reference](actions/list-deal-fields.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/boardCRM/latest/actions/list-deal-fields).

## Change Deal Column

Moves deals between columns in BoardCRM.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/change-deal-column" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "columnIdFrom": 1,
  "columnIdTo": 1,
  "ids[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/change-deal-column', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "columnIdFrom": 1,
    "columnIdTo": 1,
    "ids[]": [1]
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
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Change Deal Column action reference](actions/change-deal-column.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/boardCRM/latest/actions/change-deal-column).
