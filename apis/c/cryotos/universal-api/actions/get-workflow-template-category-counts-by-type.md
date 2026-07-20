# Cryotos: Get Workflow Template Category Counts By Type



```
GET https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/get-workflow-template-category-counts-by-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryotos `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/get-workflow-template-category-counts-by-type?connectionId=$CONNECTION_ID&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/get-workflow-template-category-counts-by-type?${params}`, {
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
| `type` | string | yes | The workflow type to summarize. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "id": 1,
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `id` | number |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Cryotos API, this operation is `GET /api/publicTemplateCategories/template-count/list-by-type/:type` (base URL `https://app.cryotos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow-template-category-counts-by-type.md) for the provider-specific parameters and requirements.

