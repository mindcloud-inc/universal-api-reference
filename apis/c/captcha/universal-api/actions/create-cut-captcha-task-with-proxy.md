# 2Captcha: Create CutCaptcha Task With Proxy

Creates a proxied CutCaptcha task in 2Captcha.

```
POST https://connect.mindcloud.co/v1/universal/captcha/latest/actions/create-cut-captcha-task-with-proxy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Captcha `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/captcha/latest/actions/create-cut-captcha-task-with-proxy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "task.websiteURL": "https://example.com",
  "task.miseryKey": "string",
  "task.apiKey": "string",
  "task.proxyType": "string",
  "task.proxyAddress": "string",
  "task.proxyPort": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/captcha/latest/actions/create-cut-captcha-task-with-proxy', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "task.websiteURL": "https://example.com",
    "task.miseryKey": "string",
    "task.apiKey": "string",
    "task.proxyType": "string",
    "task.proxyAddress": "string",
    "task.proxyPort": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `task.websiteURL` | string | yes |  |
| `task.miseryKey` | string | yes |  |
| `task.apiKey` | string | yes |  |
| `task.proxyType` | string | yes | Proxy type: http, socks4, or socks5. |
| `task.proxyAddress` | string | yes | Proxy IP address or hostname. |
| `task.proxyPort` | number | yes | Proxy port. |
| `task.proxyLogin` | string | no | Proxy login for basic authentication. |
| `task.proxyPassword` | string | no | Proxy password for basic authentication. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorId": 1,
      "taskId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorId` | number | 2Captcha error id. 0 means success. |
| `taskId` | number | Created 2Captcha task id. |

## Native endpoint

Through the native 2Captcha API, this operation is `POST /createTask` (base URL `https://api.2captcha.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-cut-captcha-task-with-proxy.md) for the provider-specific parameters and requirements.

