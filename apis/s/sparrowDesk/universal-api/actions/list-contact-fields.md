# SparrowDesk: List Contact Fields

Retrieves contact fields from SparrowDesk.

```
GET https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/list-contact-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparrowDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/list-contact-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/list-contact-fields?${params}`, {
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
      "createdAt": "string",
      "deletedAt": "string",
      "description": "string",
      "id": 1,
      "internalName": "Ava Chen",
      "isActive": true,
      "isDefault": true,
      "meta": {
        "hasNextPage": true,
        "total": 1
      },
      "name": "Ava Chen",
      "properties": {},
      "required": true,
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Creation timestamp. |
| `deletedAt` | string | Deletion timestamp when present. |
| `description` | string | Field description. |
| `id` | number | Contact field ID. |
| `internalName` | string | Internal field key. |
| `isActive` | boolean | Whether the field is active. |
| `isDefault` | boolean | Whether the field is a default field. |
| `meta.hasNextPage` | boolean | Whether another page exists. |
| `meta.total` | number | Total number of fields. |
| `name` | string | Field label. |
| `properties` | object | Additional field properties. |
| `required` | boolean | Whether the field is required. |
| `type` | string | Field type. |
| `updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native SparrowDesk API, this operation is `GET /contact-fields` (base URL `https://api.sparrowdesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-fields.md) for the provider-specific parameters and requirements.

