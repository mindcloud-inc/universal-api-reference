# Hoversignal: Test API Key Authentication



```
GET https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/test-api-key-authentication
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hoversignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/test-api-key-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/test-api-key-authentication?${params}`, {
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
      "siteDomain": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `siteDomain` | string | The Hoversignal site domain associated with the authenticated API key. |
| `success` | boolean | Whether the API key is valid for the current Hoversignal site. |

## Native endpoint

Through the native Hoversignal API, this operation is `GET /api/v1/test` (base URL `https://app.hoversignal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-api-key-authentication.md) for the provider-specific parameters and requirements.

