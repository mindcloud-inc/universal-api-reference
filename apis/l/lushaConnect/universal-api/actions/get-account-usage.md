# Lusha Connect: Get Account Usage

Retrieves account usage statistics from Lusha Connect.

```
GET https://connect.mindcloud.co/v1/universal/lushaConnect/latest/actions/get-account-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lusha Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lushaConnect/latest/actions/get-account-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lushaConnect/latest/actions/get-account-usage?${params}`, {
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
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `usage` | object | Account usage statistics keyed by credit bucket. |

## Native endpoint

Through the native Lusha Connect API, this operation is `GET /account/usage` (base URL `https://api.lusha.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-usage.md) for the provider-specific parameters and requirements.

