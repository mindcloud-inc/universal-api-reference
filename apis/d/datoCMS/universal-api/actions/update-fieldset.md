# DatoCMS: Update Fieldset



```
PUT https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/update-fieldset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/update-fieldset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fieldsetId": "string",
  "attributes": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/update-fieldset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fieldsetId": "string",
    "attributes": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fieldsetId` | string | yes | Fieldset ID. |
| `attributes` | object | yes | Fieldset attributes payload. Example: `[object Object]`. |
| `attributes.title` | string | no |  |
| `attributes.hint` | string | no |  |
| `attributes.position` | number | no |  |
| `attributes.collapsible` | boolean | no |  |
| `attributes.startCollapsed` | boolean | no |  |

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

Through the native DatoCMS API, this operation is `PUT /fieldsets/:fieldsetId` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-fieldset.md) for the provider-specific parameters and requirements.

