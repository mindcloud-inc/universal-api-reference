# Laposta: Create Field

Creates a custom field in Laposta.

```
POST https://connect.mindcloud.co/v1/universal/laposta/latest/actions/create-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Laposta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/laposta/latest/actions/create-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string",
  "name": "Ava Chen",
  "datatype": "date",
  "required": true,
  "inForm": true,
  "inList": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/laposta/latest/actions/create-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string",
    "name": "Ava Chen",
    "datatype": "date",
    "required": true,
    "inForm": true,
    "inList": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes | The ID of the list that will own the field. |
| `name` | string | yes | Field name. |
| `defaultValue` | string | no | Default field value. |
| `datatype` | list | yes | Supported simple field type. One of: `date`, `numeric`, `text`. |
| `required` | boolean | yes | Whether the field is required. |
| `inForm` | boolean | yes | Whether the field appears in the signup form. |
| `inList` | boolean | yes | Whether the field is visible in the Laposta overview. |

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

Through the native Laposta API, this operation is `POST /field` (base URL `https://api.laposta.nl/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-field.md) for the provider-specific parameters and requirements.

