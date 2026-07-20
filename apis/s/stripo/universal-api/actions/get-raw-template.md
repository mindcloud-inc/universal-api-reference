# Stripo: Get Raw Template

Retrieves raw HTML and CSS for a template from Stripo.

```
GET https://connect.mindcloud.co/v1/universal/stripo/latest/actions/get-raw-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripo/latest/actions/get-raw-template?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripo/latest/actions/get-raw-template?${params}`, {
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
| `id` | number | yes | The template ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "css": "string",
      "html": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `css` | string | Raw template CSS returned by Stripo. |
| `html` | string | Raw template HTML returned by Stripo. |

## Native endpoint

Through the native Stripo API, this operation is `GET /raw-template/:id` (base URL `https://my.stripo.email/emailgeneration/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-raw-template.md) for the provider-specific parameters and requirements.

