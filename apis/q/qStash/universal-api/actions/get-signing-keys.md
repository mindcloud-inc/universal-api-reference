# QStash: Get Signing Keys

Retrieves the current signing keys from QStash.

```
GET https://connect.mindcloud.co/v1/universal/qStash/latest/actions/get-signing-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QStash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qStash/latest/actions/get-signing-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qStash/latest/actions/get-signing-keys?${params}`, {
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
      "current": "string",
      "next": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current` | string |  |
| `next` | string |  |

## Native endpoint

Through the native QStash API, this operation is `GET /v2/keys` (base URL `https://qstash-eu-central-1.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signing-keys.md) for the provider-specific parameters and requirements.

