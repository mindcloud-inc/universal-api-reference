# ScrapFly: Download Screenshot

Retrieves a screenshot attachment from ScrapFly.

```
GET https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/download-screenshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapFly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/download-screenshot?connectionId=$CONNECTION_ID&screenshotId=01HZX8ABCDEFG1234567890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "screenshotId": "01HZX8ABCDEFG1234567890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/download-screenshot?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `screenshotId` | string | yes | Screenshot identifier returned by ScrapFly. Example: `01HZX8ABCDEFG1234567890`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ScrapFly API returns.

## Native endpoint

Through the native ScrapFly API, this operation is `GET /screenshot/:screenshotId/main` (base URL `https://api.scrapfly.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-screenshot.md) for the provider-specific parameters and requirements.

