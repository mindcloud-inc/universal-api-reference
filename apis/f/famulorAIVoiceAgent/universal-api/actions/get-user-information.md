# Famulor AI - Voice Agent: Get User Information

Retrieves the authenticated user's account details from Famulor.

```
GET https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/get-user-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Famulor AI - Voice Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/get-user-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/get-user-information?${params}`, {
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
      "email": "ava@example.com",
      "name": "Ava Chen",
      "total_balance": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Account email address. |
| `name` | string | Account user name. |
| `total_balance` | number | Current account balance. |

## Native endpoint

Through the native Famulor AI - Voice Agent API, this operation is `GET /user/me` (base URL `https://app.famulor.de/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-information.md) for the provider-specific parameters and requirements.

