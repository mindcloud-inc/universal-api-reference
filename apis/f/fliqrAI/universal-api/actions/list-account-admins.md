# Fliqr AI: List Account Admins

Retrieves account admins from Fliqr AI.

```
GET https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/list-account-admins
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fliqr AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/list-account-admins?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/list-account-admins?${params}`, {
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
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "googleBmId": "string",
      "id": "string",
      "instagramId": "string",
      "lastName": "Chen",
      "messengerId": "string",
      "profilePic": "string",
      "smsId": "string",
      "telegramId": "string",
      "viberId": "string",
      "whatsappId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `googleBmId` | string |  |
| `id` | string |  |
| `instagramId` | string |  |
| `lastName` | string |  |
| `messengerId` | string |  |
| `profilePic` | string |  |
| `smsId` | string |  |
| `telegramId` | string |  |
| `viberId` | string |  |
| `whatsappId` | string |  |

## Native endpoint

Through the native Fliqr AI API, this operation is `GET /accounts/admins` (base URL `https://app.fliqr.ai/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-account-admins.md) for the provider-specific parameters and requirements.

