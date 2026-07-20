# TelTel: Lookup Phone Numbers

Looks up phone numbers in TelTel.

```
GET https://connect.mindcloud.co/v1/universal/telTel/latest/actions/lookup-phone-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TelTel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/telTel/latest/actions/lookup-phone-numbers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/telTel/latest/actions/lookup-phone-numbers?${params}`, {
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
      "country": "string",
      "number": "string",
      "operator": "string",
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `number` | string |  |
| `operator` | string |  |
| `valid` | boolean |  |

## Native endpoint

Through the native TelTel API, this operation is `GET /numbers/lookup/{numbers}` (base URL `https://api.teltel.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-phone-numbers.md) for the provider-specific parameters and requirements.

