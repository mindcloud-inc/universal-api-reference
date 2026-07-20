# Toolhouse: Convert Text to Cron



```
GET https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/convert-text-to-cron
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toolhouse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/convert-text-to-cron?connectionId=$CONNECTION_ID&cron=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cron": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/convert-text-to-cron?${params}`, {
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
| `cron` | string | yes | A natural-language scheduling prompt to convert into cron. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string |  |

## Native endpoint

Through the native Toolhouse API, this operation is `GET /schedules/text-to-cron` (base URL `https://api.toolhouse.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-text-to-cron.md) for the provider-specific parameters and requirements.

