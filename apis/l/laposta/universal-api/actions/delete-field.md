# Laposta: Delete Field

Deletes an existing custom field from Laposta.

```
DELETE https://connect.mindcloud.co/v1/universal/laposta/latest/actions/delete-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Laposta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/laposta/latest/actions/delete-field?connectionId=$CONNECTION_ID&fieldId=string&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fieldId": "string",
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/laposta/latest/actions/delete-field?${params}`, {
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
| `fieldId` | string | yes | The ID of the field to delete. |
| `listId` | string | yes | The ID of the list that owns the field. |

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

Through the native Laposta API, this operation is `DELETE /field/:fieldId` (base URL `https://api.laposta.nl/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-field.md) for the provider-specific parameters and requirements.

