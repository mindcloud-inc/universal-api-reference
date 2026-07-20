# Billwerkplus: Get Account

Retrieves current account details from Billwerkplus.

```
GET https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/get-current-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billwerkplus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/get-current-account?${params}`, {
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
      "created": "string",
      "currency": "string",
      "defaultVat": 1,
      "email": "ava@example.com",
      "handle": "string",
      "id": "string",
      "locale": "string",
      "name": "Ava Chen",
      "organisation": "string",
      "state": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `created` | string |  |
| `currency` | string |  |
| `defaultVat` | number |  |
| `email` | string |  |
| `handle` | string |  |
| `id` | string |  |
| `locale` | string |  |
| `name` | string |  |
| `organisation` | string |  |
| `state` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native Billwerkplus API, this operation is `GET /account` (base URL `https://api.frisbii.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-account.md) for the provider-specific parameters and requirements.

