# Monica CRM: List Contact Field Types

Retrieves contact field types from Monica CRM.

```
GET https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/list-contact-field-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monica CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/list-contact-field-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/list-contact-field-types?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Monica CRM API, this operation is `GET /contactfieldtypes` (base URL `https://app.monicahq.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-field-types.md) for the provider-specific parameters and requirements.

