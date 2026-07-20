# JustSift: List Person Fields



```
GET https://connect.mindcloud.co/v1/universal/justSift/latest/actions/list-person-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JustSift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/justSift/latest/actions/list-person-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/justSift/latest/actions/list-person-fields?${params}`, {
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
      "displayName": "Ava Chen",
      "filterable": true,
      "id": "string",
      "objectKey": "string",
      "searchable": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string | Human-readable field name. |
| `filterable` | boolean | Whether this field can be used as a search filter. |
| `id` | string | Unique field identifier. |
| `objectKey` | string | Property name on the Person object. |
| `searchable` | boolean | Whether this field is searched by generic search terms. |
| `type` | string | Sift field type. |

## Native endpoint

Through the native JustSift API, this operation is `GET /fields/person` (base URL `https://api.justsift.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-person-fields.md) for the provider-specific parameters and requirements.

