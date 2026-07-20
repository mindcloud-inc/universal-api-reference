# Laposta: Update Field

Updates an existing custom field in Laposta.

```
PUT https://connect.mindcloud.co/v1/universal/laposta/latest/actions/update-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Laposta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/laposta/latest/actions/update-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fieldId": "string",
  "listId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/laposta/latest/actions/update-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fieldId": "string",
    "listId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fieldId` | string | yes | The ID of the field to update. |
| `listId` | string | yes | The ID of the list that owns the field. |
| `name` | string | no | Updated field name. |
| `defaultValue` | string | no | Updated default field value. |
| `datatype` | list | no | Updated supported simple field type. One of: `date`, `numeric`, `text`. |
| `required` | boolean | no | Whether the field is required. |
| `inForm` | boolean | no | Whether the field appears in the signup form. |
| `inList` | boolean | no | Whether the field is visible in the Laposta overview. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field": {
        "datatype": "string",
        "defaultValue": "string",
        "fieldId": "string",
        "inForm": true,
        "inList": true,
        "listId": "string",
        "name": "Ava Chen",
        "required": true,
        "state": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field` | object |  |
| `field.datatype` | string |  |
| `field.defaultValue` | string |  |
| `field.fieldId` | string |  |
| `field.inForm` | boolean |  |
| `field.inList` | boolean |  |
| `field.listId` | string |  |
| `field.name` | string |  |
| `field.required` | boolean |  |
| `field.state` | string |  |

## Native endpoint

Through the native Laposta API, this operation is `POST /field/:fieldId` (base URL `https://api.laposta.nl/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-field.md) for the provider-specific parameters and requirements.

