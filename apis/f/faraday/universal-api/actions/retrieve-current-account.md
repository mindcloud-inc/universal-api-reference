# Faraday: Retrieve Current Account

Retrieves the current account from Faraday.

```
GET https://connect.mindcloud.co/v1/universal/faraday/latest/actions/retrieve-current-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Faraday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/faraday/latest/actions/retrieve-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/faraday/latest/actions/retrieve-current-account?${params}`, {
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
      "apiKey": "string",
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "parentAccountId": "string",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKey` | string | Faraday API key returned by the provider. |
| `createdAt` | string | Creation timestamp. |
| `id` | string | Faraday account ID. |
| `name` | string | Account name. |
| `parentAccountId` | string | Parent account ID. |
| `status` | string | Account status. |
| `updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native Faraday API, this operation is `GET /accounts/current` (base URL `https://api.faraday.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-current-account.md) for the provider-specific parameters and requirements.

