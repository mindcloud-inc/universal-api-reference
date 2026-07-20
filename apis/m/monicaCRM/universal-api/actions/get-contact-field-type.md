# Monica CRM: Get Contact Field Type

Retrieves a contact field type from Monica CRM.

```
GET https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/get-contact-field-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monica CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/get-contact-field-type?connectionId=$CONNECTION_ID&contactFieldTypeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactFieldTypeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/get-contact-field-type?${params}`, {
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
| `contactFieldTypeId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "created_at": "string",
        "delible": true,
        "fontawesome_icon": "string",
        "id": 1,
        "name": "Ava Chen",
        "object": "string",
        "protocol": "string",
        "type": "string",
        "updated_at": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.created_at` | string |  |
| `data.delible` | boolean |  |
| `data.fontawesome_icon` | string |  |
| `data.id` | number |  |
| `data.name` | string |  |
| `data.object` | string |  |
| `data.protocol` | string |  |
| `data.type` | string |  |
| `data.updated_at` | string |  |

## Native endpoint

Through the native Monica CRM API, this operation is `GET /contactfieldtypes/:contactFieldTypeId` (base URL `https://app.monicahq.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-field-type.md) for the provider-specific parameters and requirements.

