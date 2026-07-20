# Quizell: List Customer Custom Fields

Retrieves customer custom fields from Quizell.

```
GET https://connect.mindcloud.co/v1/universal/quizell/latest/actions/list-customer-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quizell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quizell/latest/actions/list-customer-custom-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quizell/latest/actions/list-customer-custom-fields?${params}`, {
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
      "field_name": "Ava Chen",
      "field_type": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field_name` | string |  |
| `field_type` | string |  |
| `id` | number |  |

## Native endpoint

Through the native Quizell API, this operation is `GET /customers/custom_fields/list` (base URL `https://api.quizell.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-custom-fields.md) for the provider-specific parameters and requirements.

