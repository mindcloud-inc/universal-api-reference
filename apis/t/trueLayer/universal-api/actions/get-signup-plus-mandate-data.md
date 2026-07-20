# TrueLayer: Get Signup Plus Mandate Data

Retrieves Signup+ mandate data from TrueLayer.

```
GET https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-signup-plus-mandate-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrueLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-signup-plus-mandate-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-signup-plus-mandate-data?${params}`, {
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
      "account_details": {},
      "address": {},
      "date_of_birth": "string",
      "first_name": "Ava",
      "last_name": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_details` | object |  |
| `address` | object |  |
| `date_of_birth` | string |  |
| `first_name` | string |  |
| `last_name` | string |  |

## Native endpoint

Through the native TrueLayer API, this operation is `GET /signup-plus/mandates` (base URL `https://api.truelayer-sandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signup-plus-mandate-data.md) for the provider-specific parameters and requirements.

