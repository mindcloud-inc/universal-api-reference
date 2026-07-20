# Evervault: Decrypt Data

Decrypts previously encrypted data with Evervault.

```
GET https://connect.mindcloud.co/v1/universal/evervault/latest/actions/decrypt-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evervault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evervault/latest/actions/decrypt-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evervault/latest/actions/decrypt-data?${params}`, {
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
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Decrypted JSON payload. Shape follows input payload. |

## Native endpoint

Through the native Evervault API, this operation is `POST /decrypt` (base URL `https://api.evervault.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/decrypt-data.md) for the provider-specific parameters and requirements.

