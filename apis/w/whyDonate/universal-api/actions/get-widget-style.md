# WhyDonate: Get Widget Style



```
GET https://connect.mindcloud.co/v1/universal/whyDonate/latest/actions/get-widget-style
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhyDonate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whyDonate/latest/actions/get-widget-style?connectionId=$CONNECTION_ID&shortcode=wd-123456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shortcode": "wd-123456"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whyDonate/latest/actions/get-widget-style?${params}`, {
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
| `shortcode` | string | yes | Widget shortcode used to fetch a saved style. Example: `wd-123456`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native WhyDonate API, this operation is `GET /fundraiser/user/style` (base URL `https://fundraiser.whydonate.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-widget-style.md) for the provider-specific parameters and requirements.

