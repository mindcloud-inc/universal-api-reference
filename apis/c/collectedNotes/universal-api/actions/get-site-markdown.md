# Collected Notes: Get Site Markdown



```
GET https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/get-site-markdown
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Collected Notes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/get-site-markdown?connectionId=$CONNECTION_ID&sitePath=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sitePath": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/get-site-markdown?${params}`, {
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
| `sitePath` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |

## Native endpoint

Through the native Collected Notes API, this operation is `GET /:sitePath.md` (base URL `https://collectednotes.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site-markdown.md) for the provider-specific parameters and requirements.

