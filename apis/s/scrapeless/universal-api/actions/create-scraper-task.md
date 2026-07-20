# Scrapeless: Create Scraper Task

Creates a new scraper task in Scrapeless.

```
POST https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/create-scraper-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/create-scraper-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actor": "string",
  "input": {},
  "input.url": "https://example.com",
  "proxy": {},
  "proxy.country": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/create-scraper-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actor": "string",
    "input": {},
    "input.url": "https://example.com",
    "proxy": {},
    "proxy.country": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actor` | string | yes |  |
| `input` | object | yes |  |
| `input.url` | string | yes |  |
| `proxy` | object | yes |  |
| `proxy.country` | string | yes |  |
| `async` | boolean | no | If true, the task will be executed asynchronously. If false, the task will be executed synchronously. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Scrapeless API returns.

## Native endpoint

Through the native Scrapeless API, this operation is `POST /api/v1/scraper/request` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-scraper-task.md) for the provider-specific parameters and requirements.

