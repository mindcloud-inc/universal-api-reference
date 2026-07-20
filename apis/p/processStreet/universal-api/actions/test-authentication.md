# Process Street: Test Authentication



```
GET https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/test-authentication
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Street `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/test-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/test-authentication?${params}`, {
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
      "apiKeyLabel": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKeyLabel` | string |  |

## Native endpoint

Through the native Process Street API, this operation is `GET /testAuth` (base URL `https://public-api.process.st/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-authentication.md) for the provider-specific parameters and requirements.

