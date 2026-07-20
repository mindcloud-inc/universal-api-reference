# Moderation API: Update Wordlist

Updates a wordlist in Moderation API.

```
PUT https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/update-wordlist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moderation API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/update-wordlist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/update-wordlist', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ID of the wordlist to update |
| `name` | string | no | New name for the wordlist |
| `key` | string | no | New key for the wordlist |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | New description for the wordlist |
| `words[]` | array<string> | no | New words for the wordlist. Replace the existing words with these new ones. Duplicate words will be ignored. |
| `strict` | boolean | no | Deprecated. Now using threshold in project settings. |

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

Through the native Moderation API API, this operation is `PUT /wordlist/:id` (base URL `https://api.moderationapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-wordlist.md) for the provider-specific parameters and requirements.

