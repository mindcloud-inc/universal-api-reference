# Yay.com: List Number Addresses

Retrieves number addresses from Yay.com.

```
GET https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-number-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yay.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-number-addresses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-number-addresses?${params}`, {
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
      "city": "string",
      "countryCode": "string",
      "countryPersonalId": "string",
      "forename": "Ava Chen",
      "isDefault": true,
      "name": "Ava Chen",
      "nickname": "Ava Chen",
      "postcode": "string",
      "premises": "string",
      "state": "string",
      "street": "string",
      "title": "string",
      "typeId": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `countryCode` | string |  |
| `countryPersonalId` | string |  |
| `forename` | string |  |
| `isDefault` | boolean |  |
| `name` | string |  |
| `nickname` | string |  |
| `postcode` | string |  |
| `premises` | string |  |
| `state` | string |  |
| `street` | string |  |
| `title` | string |  |
| `typeId` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native Yay.com API, this operation is `GET /voip/number-address` (base URL `https://api.yay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-number-addresses.md) for the provider-specific parameters and requirements.

