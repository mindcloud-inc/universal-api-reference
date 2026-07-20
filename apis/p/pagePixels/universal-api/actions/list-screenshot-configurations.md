# PagePixels: List Screenshot Configurations



```
GET https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/list-screenshot-configurations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PagePixels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/list-screenshot-configurations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/list-screenshot-configurations?${params}`, {
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
| `page` | number | no | The result page to retrieve. |
| `limit` | number | no | The number of records to retrieve. |
| `after` | number | no | Only include records created after this unix timestamp. |
| `before` | number | no | Only include records created before this unix timestamp. |
| `order` | string | no | Sort order, either ASC or DESC. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "createdAt": "string",
      "host": "string",
      "id": "string",
      "ids": {},
      "isBrowserExtensionScreenshot": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object | The nested screenshot configuration settings for each listed configuration. |
| `createdAt` | string | The creation timestamp returned by PagePixels. |
| `host` | string | The host or URL tracked by the configuration. |
| `id` | string | The screenshot configuration ID. |
| `ids` | object | The nested ID bundle returned by PagePixels, including embed URL and last job ID. |
| `isBrowserExtensionScreenshot` | boolean | Whether the configuration originated from the browser extension flow. |

## Native endpoint

Through the native PagePixels API, this operation is `GET /screenshot_configs` (base URL `https://api.pagepixels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-screenshot-configurations.md) for the provider-specific parameters and requirements.

