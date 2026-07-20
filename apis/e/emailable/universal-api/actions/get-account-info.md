# Emailable: Get Account Info

Retrieves account information from Emailable.

```
GET https://connect.mindcloud.co/v1/universal/emailable/latest/actions/get-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emailable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailable/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailable/latest/actions/get-account-info?${params}`, {
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
      "availableCredits": 1,
      "ownerEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableCredits` | number | The number of verification credits currently available. |
| `ownerEmail` | string | The email address that owns the Emailable account. |

## Native endpoint

Through the native Emailable API, this operation is `GET /v1/account` (base URL `https://api.emailable.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-info.md) for the provider-specific parameters and requirements.

