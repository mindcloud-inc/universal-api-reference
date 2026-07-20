# Mona AI: Check API Key Validity

Checks whether a Mona AI API key is valid.

```
GET https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/check-api-key-validity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mona AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/check-api-key-validity?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/check-api-key-validity?${params}`, {
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
      "message": "string",
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Validation status message from Mona. |
| `valid` | boolean | Whether the configured Mona API key is valid. |

## Native endpoint

Through the native Mona AI API, this operation is `POST /auth/checkIfAPIKeyIsValid` (base URL `https://api.mona-ai.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-api-key-validity.md) for the provider-specific parameters and requirements.

