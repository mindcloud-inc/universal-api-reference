# Prembly: Basic Phone Number

Creates a basic phone number verification in Prembly.

```
POST https://connect.mindcloud.co/v1/universal/prembly/latest/actions/basic-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/basic-phone-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prembly/latest/actions/basic-phone-number', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "carrier": "string",
      "country": "string",
      "is_valid": true,
      "line_type": "string",
      "owner_name": "Ava Chen",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier` | string |  |
| `country` | string |  |
| `is_valid` | boolean |  |
| `line_type` | string |  |
| `owner_name` | string |  |
| `phone` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `POST /verification/phone_number` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/basic-phone-number.md) for the provider-specific parameters and requirements.

