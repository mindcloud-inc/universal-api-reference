# Selzy: List Contact Fields

Retrieves contact fields from Selzy.

```
GET https://connect.mindcloud.co/v1/universal/selzy/latest/actions/list-contact-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Selzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/selzy/latest/actions/list-contact-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/selzy/latest/actions/list-contact-fields?${params}`, {
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
      "result": [
        {
          "id": 1,
          "is_visible": 1,
          "name": "Ava Chen",
          "public_name": "Ava Chen",
          "type": "string",
          "view_pos": 1
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
| `result[].id` | number |  |
| `result[].is_visible` | number |  |
| `result[].name` | string |  |
| `result[].public_name` | string |  |
| `result[].type` | string |  |
| `result[].view_pos` | number |  |

## Native endpoint

Through the native Selzy API, this operation is `POST getFields` (base URL `https://api.selzy.com/en/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-fields.md) for the provider-specific parameters and requirements.

