# DatoCMS: Delete Fieldset



```
DELETE https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/delete-fieldset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/delete-fieldset?connectionId=$CONNECTION_ID&fieldsetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fieldsetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/delete-fieldset?${params}`, {
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
| `fieldsetId` | string | yes | Fieldset ID. |

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

Through the native DatoCMS API, this operation is `DELETE /fieldsets/:fieldsetId` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-fieldset.md) for the provider-specific parameters and requirements.

