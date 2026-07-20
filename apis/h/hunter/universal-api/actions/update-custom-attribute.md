# Hunter: Update Custom Attribute



```
PUT https://connect.mindcloud.co/v1/universal/hunter/latest/actions/update-custom-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hunter/latest/actions/update-custom-attribute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customAttributeId": "string",
  "label": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hunter/latest/actions/update-custom-attribute', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customAttributeId": "string",
    "label": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customAttributeId` | string | yes | Identifier of the custom attribute. |
| `label` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "label": "string",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `label` | string |  |
| `slug` | string |  |

## Native endpoint

Through the native Hunter API, this operation is `PUT /leads_custom_attributes/:customAttributeId` (base URL `https://api.hunter.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-custom-attribute.md) for the provider-specific parameters and requirements.

