# DatoCMS: List Model Fieldsets



```
GET https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/list-model-fieldsets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/list-model-fieldsets?connectionId=$CONNECTION_ID&modelIdOrApiKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelIdOrApiKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/list-model-fieldsets?${params}`, {
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
| `modelIdOrApiKey` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "collapsible": true,
        "hint": "string",
        "position": 1,
        "title": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.collapsible` | boolean |  |
| `attributes.hint` | string |  |
| `attributes.position` | number |  |
| `attributes.title` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native DatoCMS API, this operation is `GET /item-types/:model_id_or_api_key/fieldsets` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-model-fieldsets.md) for the provider-specific parameters and requirements.

