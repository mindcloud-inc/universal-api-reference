# 2Captcha Universal API Examples

These examples use the MindCloud API key and 2Captcha connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Balance

Retrieves your current 2Captcha account balance.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/captcha/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/captcha/latest/actions/get-balance?${params}`, {
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
      "balance": 1,
      "errorId": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Balance action reference](actions/get-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/captcha/latest/actions/get-balance).

## Create Amazon WAF Task Proxyless

Creates a proxyless Amazon WAF captcha task in 2Captcha.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/captcha/latest/actions/create-amazon-waf-task-proxyless" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "task.websiteURL": "https://example.com",
  "task.websiteKey": "string",
  "task.iv": "string",
  "task.context": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/captcha/latest/actions/create-amazon-waf-task-proxyless', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "task.websiteURL": "https://example.com",
    "task.websiteKey": "string",
    "task.iv": "string",
    "task.context": "string"
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
      "errorId": 1,
      "taskId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Amazon WAF Task Proxyless action reference](actions/create-amazon-waf-task-proxyless.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/captcha/latest/actions/create-amazon-waf-task-proxyless).
