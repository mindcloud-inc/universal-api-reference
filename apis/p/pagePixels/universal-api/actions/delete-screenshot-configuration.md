# PagePixels: Delete Screenshot Configuration



```
DELETE https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/delete-screenshot-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PagePixels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/delete-screenshot-configuration?connectionId=$CONNECTION_ID&screenshotConfigurationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "screenshotConfigurationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/delete-screenshot-configuration?${params}`, {
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
| `screenshotConfigurationId` | string | yes | The screenshot configuration ID to delete. |

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
| `config` | object | The nested screenshot configuration settings for the deleted configuration. |
| `createdAt` | string | The creation timestamp returned by PagePixels. |
| `host` | string | The host or URL tracked by the deleted configuration. |
| `id` | string | The deleted screenshot configuration ID. |
| `ids` | object | The nested ID bundle returned by PagePixels, including embed URL and last job ID. |
| `isBrowserExtensionScreenshot` | boolean | Whether the deleted configuration originated from the browser extension flow. |

## Native endpoint

Through the native PagePixels API, this operation is `DELETE /screenshot_configs/:screenshot_config_id` (base URL `https://api.pagepixels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-screenshot-configuration.md) for the provider-specific parameters and requirements.

