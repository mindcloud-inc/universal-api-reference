# EasyContent: List Template Content Items

Retrieves EasyContent items that use a specific template.

```
GET https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/list-template-content-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/list-template-content-items?connectionId=$CONNECTION_ID&templateId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/list-template-content-items?${params}`, {
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
| `templateId` | number | yes |  |
| `title` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native EasyContent API, this operation is `GET /v2/content/templates/:templateId/content-items` (base URL `https://easycontent.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-template-content-items.md) for the provider-specific parameters and requirements.

