# TelTel: Update Phone Number

Updates an existing phone number in TelTel.

```
PUT https://connect.mindcloud.co/v1/universal/telTel/latest/actions/update-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TelTel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/telTel/latest/actions/update-phone-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/telTel/latest/actions/update-phone-number', {
  method: 'PUT',
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
      "autoRenew": true,
      "description": "string",
      "id": 1,
      "phoneNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoRenew` | boolean |  |
| `description` | string |  |
| `id` | number |  |
| `phoneNumber` | string |  |

## Native endpoint

Through the native TelTel API, this operation is `PATCH /dids/my-numbers/{id}` (base URL `https://api.teltel.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-phone-number.md) for the provider-specific parameters and requirements.

