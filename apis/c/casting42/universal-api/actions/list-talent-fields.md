# Casting42: List Talent Fields

Retrieves available talent fields from Casting42.

```
GET https://connect.mindcloud.co/v1/universal/casting42/latest/actions/list-talent-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Casting42 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/casting42/latest/actions/list-talent-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/casting42/latest/actions/list-talent-fields?${params}`, {
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
      "choices": [
        {}
      ],
      "list": true,
      "name": "Ava Chen",
      "required": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `choices` | array<object> | Available choices for list-backed fields when present. |
| `list` | boolean | Whether the field supports multiple selections. |
| `name` | string | Talent field label. |
| `required` | boolean | Whether the field is required in Casting42. |
| `type` | string | Casting42 field type. |

## Native endpoint

Through the native Casting42 API, this operation is `GET /api/v2/settings/fields` (base URL `https://casting42.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-talent-fields.md) for the provider-specific parameters and requirements.

