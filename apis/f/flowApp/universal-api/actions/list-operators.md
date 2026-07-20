# Flow App: List Operators



```
GET https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/list-operators
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/list-operators?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/list-operators?${params}`, {
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
      "accountServiceLevel": 1,
      "accountToken": "string",
      "avatarExtension": "string",
      "avatarToken": "string",
      "bio": "string",
      "company": "string",
      "createdBy": 1,
      "createdDate": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "linkedinUrl": "https://example.com",
      "permission": 1,
      "phone": "string",
      "title": "string",
      "token": "string",
      "twitterID": "string",
      "userID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountServiceLevel` | number | Flow account service level. |
| `accountToken` | string | Flow account token associated with the operator. |
| `avatarExtension` | string | Avatar file extension if present. |
| `avatarToken` | string | Avatar token if present. |
| `bio` | string | Operator bio text. |
| `company` | string | Operator company name. |
| `createdBy` | number | Creator user ID. |
| `createdDate` | number | Unix timestamp when the operator record was created. |
| `email` | string | Operator email address. |
| `firstName` | string | Operator first name. |
| `id` | number | Operator user ID. |
| `lastName` | string | Operator last name. |
| `linkedinUrl` | string | Operator LinkedIn URL if present. |
| `permission` | number | Operator permission level. |
| `phone` | string | Operator phone number. |
| `title` | string | Operator title. |
| `token` | string | Flow token for the operator. |
| `twitterID` | string | Operator Twitter ID if present. |
| `userID` | number | Flow user ID for the operator. |

## Native endpoint

Through the native Flow App API, this operation is `GET /users` (base URL `https://prod.flowapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-operators.md) for the provider-specific parameters and requirements.

