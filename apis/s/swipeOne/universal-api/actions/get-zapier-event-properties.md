# Swipe One: Get Zapier Event Properties



```
GET https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/get-zapier-event-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swipe One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/get-zapier-event-properties?connectionId=$CONNECTION_ID&event=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "event": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/get-zapier-event-properties?${params}`, {
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
| `event` | string | yes | Event identifier to retrieve properties for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string",
      "label": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string |  |
| `label` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Swipe One API, this operation is `GET /zapier/events/:event` (base URL `https://api.swipeone.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-zapier-event-properties.md) for the provider-specific parameters and requirements.

