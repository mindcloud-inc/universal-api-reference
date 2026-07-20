# TelTel: List Phone Numbers

Retrieves phone numbers from your TelTel account.

```
GET https://connect.mindcloud.co/v1/universal/telTel/latest/actions/list-phone-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TelTel `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/telTel/latest/actions/list-phone-numbers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/telTel/latest/actions/list-phone-numbers?${params}`, {
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

Through the native TelTel API, this operation is `GET /dids/my-numbers` (base URL `https://api.teltel.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-phone-numbers.md) for the provider-specific parameters and requirements.

