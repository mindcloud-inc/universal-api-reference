# Crisp: Get Website Operator

Retrieves a website operator from Crisp.

```
GET https://connect.mindcloud.co/v1/universal/crisp/latest/actions/get-website-operator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crisp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crisp/latest/actions/get-website-operator?connectionId=$CONNECTION_ID&websiteId=string&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crisp/latest/actions/get-website-operator?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `websiteId` | string | yes | The website identifier |
| `userId` | string | yes | The user identifier for operator |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availability": "string",
      "avatar": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "hasToken": true,
      "lastName": "Chen",
      "role": "string",
      "title": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availability` | string |  |
| `avatar` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `hasToken` | boolean |  |
| `lastName` | string |  |
| `role` | string |  |
| `title` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Crisp API, this operation is `GET /website/:website_id/operator/:user_id` (base URL `https://api.crisp.chat/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-website-operator.md) for the provider-specific parameters and requirements.

