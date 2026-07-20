# Qase: Get all System Fields

Retrieves system fields from Qase.

```
GET https://connect.mindcloud.co/v1/universal/qase/latest/actions/get-system-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qase/latest/actions/get-system-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qase/latest/actions/get-system-fields?${params}`, {
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
      "default_value": "string",
      "entity": 1,
      "is_required": true,
      "options": [
        {}
      ],
      "slug": "string",
      "title": "string",
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `default_value` | string |  |
| `entity` | number |  |
| `is_required` | boolean |  |
| `options` | array<object> |  |
| `slug` | string |  |
| `title` | string |  |
| `type` | number |  |

## Native endpoint

Through the native Qase API, this operation is `GET /system_field` (base URL `https://api.qase.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-system-fields.md) for the provider-specific parameters and requirements.

