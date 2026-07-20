# DatoCMS: Create Fieldset



```
POST https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/create-fieldset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/create-fieldset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemTypeId": "string",
  "title": "SEO"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/create-fieldset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemTypeId": "string",
    "title": "SEO"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemTypeId` | string | yes | Model ID or API key. |
| `title` | string | yes | Fieldset title. Example: `SEO`. |

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
        "startCollapsed": true,
        "title": "string"
      },
      "id": "string",
      "relationships": {
        "itemType": {
          "data": {
            "id": "string",
            "type": "string"
          }
        }
      },
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
| `attributes.startCollapsed` | boolean |  |
| `attributes.title` | string |  |
| `id` | string |  |
| `relationships.itemType.data.id` | string |  |
| `relationships.itemType.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native DatoCMS API, this operation is `POST /item-types/:itemTypeId/fieldsets` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-fieldset.md) for the provider-specific parameters and requirements.

