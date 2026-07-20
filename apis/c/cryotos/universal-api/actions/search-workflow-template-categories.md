# Cryotos: Search Workflow Template Categories



```
GET https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/search-workflow-template-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryotos `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/search-workflow-template-categories?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/search-workflow-template-categories?${params}`, {
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
| `text` | string | yes | The workflow template category search text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "creationDate": "string",
      "id": 1,
      "name": "Ava Chen",
      "s3ImageId": "string",
      "signedUrl": "https://example.com",
      "updationDate": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `creationDate` | string |  |
| `id` | number |  |
| `name` | string |  |
| `s3ImageId` | string |  |
| `signedUrl` | string |  |
| `updationDate` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Cryotos API, this operation is `GET /api/publicTemplateCategories/_search/:text` (base URL `https://app.cryotos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-workflow-template-categories.md) for the provider-specific parameters and requirements.

