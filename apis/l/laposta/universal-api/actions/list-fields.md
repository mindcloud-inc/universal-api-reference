# Laposta: List Fields

Retrieves custom fields from Laposta.

```
GET https://connect.mindcloud.co/v1/universal/laposta/latest/actions/list-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Laposta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/laposta/latest/actions/list-fields?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/laposta/latest/actions/list-fields?${params}`, {
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
| `listId` | string | yes | The ID of the list whose fields to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "field": {
            "datatype": "string",
            "fieldId": "string",
            "name": "Ava Chen",
            "required": true
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].field` | object |  |
| `data[].field.datatype` | string |  |
| `data[].field.fieldId` | string |  |
| `data[].field.name` | string |  |
| `data[].field.required` | boolean |  |

## Native endpoint

Through the native Laposta API, this operation is `GET /field` (base URL `https://api.laposta.nl/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fields.md) for the provider-specific parameters and requirements.

