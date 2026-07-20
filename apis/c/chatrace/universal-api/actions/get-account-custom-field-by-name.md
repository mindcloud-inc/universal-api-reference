# Chatrace: Get Account Custom Field By Name

Finds an account custom field in Chatrace by name.

```
GET https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/get-account-custom-field-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatrace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/get-account-custom-field-by-name?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/get-account-custom-field-by-name?${params}`, {
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
      "name": "Ava Chen",
      "type": 1
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
| `name` | string |  |
| `type` | number |  |

## Native endpoint

Through the native Chatrace API, this operation is `GET /accounts/custom_fields/name/:custom_field_name` (base URL `https://api.chatrace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-custom-field-by-name.md) for the provider-specific parameters and requirements.

