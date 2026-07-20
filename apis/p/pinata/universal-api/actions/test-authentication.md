# Pinata: Test Authentication

Retrieves the current authentication status from Pinata.

```
GET https://connect.mindcloud.co/v1/universal/pinata/latest/actions/test-authentication
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinata/latest/actions/test-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinata/latest/actions/test-authentication?${params}`, {
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Authentication test confirmation message. |

## Native endpoint

Through the native Pinata API, this operation is `GET /data/testAuthentication` (base URL `https://api.pinata.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-authentication.md) for the provider-specific parameters and requirements.

