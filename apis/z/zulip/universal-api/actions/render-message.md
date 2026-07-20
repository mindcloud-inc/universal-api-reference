# Zulip: Render Message

Renders Zulip message content into HTML.

```
GET https://connect.mindcloud.co/v1/universal/zulip/latest/actions/render-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zulip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zulip/latest/actions/render-message?connectionId=$CONNECTION_ID&content=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "content": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zulip/latest/actions/render-message?${params}`, {
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
| `content` | string | yes | The Markdown message content to render. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "msg": "string",
      "rendered": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `msg` | string |  |
| `rendered` | string |  |
| `result` | string |  |

## Native endpoint

Through the native Zulip API, this operation is `POST /messages/render` (base URL `{{credentials.site}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/render-message.md) for the provider-specific parameters and requirements.

