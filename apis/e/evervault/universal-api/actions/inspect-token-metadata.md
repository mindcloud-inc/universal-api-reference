# Evervault: Inspect Token Metadata

Retrieves metadata for an encrypted token from Evervault.

```
GET https://connect.mindcloud.co/v1/universal/evervault/latest/actions/inspect-token-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evervault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evervault/latest/actions/inspect-token-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evervault/latest/actions/inspect-token-metadata?${params}`, {
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
      "category": "string",
      "encryptedAt": 1,
      "fingerprint": "string",
      "metadata": {},
      "role": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `encryptedAt` | number |  |
| `fingerprint` | string |  |
| `metadata` | object |  |
| `role` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Evervault API, this operation is `POST /inspect` (base URL `https://api.evervault.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/inspect-token-metadata.md) for the provider-specific parameters and requirements.

