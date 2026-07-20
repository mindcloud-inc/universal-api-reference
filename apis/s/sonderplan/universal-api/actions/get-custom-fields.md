# Sonderplan: Get Custom Fields



```
GET https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sonderplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-custom-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-custom-fields?${params}`, {
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
      "description": "string",
      "id": 1,
      "module": "string",
      "name": "Ava Chen",
      "order": 1,
      "required": true,
      "type": "string",
      "updateKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | number |  |
| `module` | string |  |
| `name` | string |  |
| `order` | number |  |
| `required` | boolean |  |
| `type` | string |  |
| `updateKey` | string |  |

## Native endpoint

Through the native Sonderplan API, this operation is `GET /custom-field` (base URL `https://api.sonderplan.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-fields.md) for the provider-specific parameters and requirements.

