# Chatrace: Get Account Integrations

Retrieves account integrations from your Chatrace account.

```
GET https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/get-account-integrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatrace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/get-account-integrations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/get-account-integrations?${params}`, {
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
      "claude": {},
      "deepseek": {},
      "email": {},
      "gemini": {},
      "google_sheets": {},
      "openai": {},
      "xai": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `claude` | object |  |
| `deepseek` | object |  |
| `email` | object |  |
| `gemini` | object |  |
| `google_sheets` | object |  |
| `openai` | object |  |
| `xai` | object |  |

## Native endpoint

Through the native Chatrace API, this operation is `GET /accounts/integrations` (base URL `https://api.chatrace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-integrations.md) for the provider-specific parameters and requirements.

