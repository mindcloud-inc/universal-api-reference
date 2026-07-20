# Moderation API: Get Wordlist

Retrieves a wordlist from Moderation API.

```
GET https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-wordlist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moderation API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-wordlist?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-wordlist?${params}`, {
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
| `id` | string | yes | ID of the wordlist to get |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "organizationId": "string",
      "strict": true,
      "userId": "string",
      "words": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Creation date of the wordlist |
| `id` | string | ID of the wordlist |
| `name` | string | Name of the wordlist |
| `organizationId` | string | ID of the organization |
| `strict` | boolean | Strict mode |
| `userId` | string | ID of the user |
| `words` | array<string> | Words in the wordlist |

## Native endpoint

Through the native Moderation API API, this operation is `GET /wordlist/:id` (base URL `https://api.moderationapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wordlist.md) for the provider-specific parameters and requirements.

