# Specific: List Conversations

Retrieves a list of conversations from Specific.

```
GET https://connect.mindcloud.co/v1/universal/specific/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Specific `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/specific/latest/actions/list-conversations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/specific/latest/actions/list-conversations?${params}`, {
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
      "company": {
        "id": "string",
        "name": "Ava Chen"
      },
      "contact": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "id": "string",
      "insertedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "plainText": "string",
      "source": {
        "id": "string",
        "name": "Ava Chen"
      },
      "sourceUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company.id` | string |  |
| `company.name` | string |  |
| `contact.email` | string |  |
| `contact.id` | string |  |
| `contact.name` | string |  |
| `id` | string |  |
| `insertedAt` | date |  |
| `name` | string |  |
| `plainText` | string |  |
| `source.id` | string |  |
| `source.name` | string |  |
| `sourceUrl` | string |  |

## Native endpoint

Through the native Specific API, this operation is `POST` (base URL `https://public-api.specific.app/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

