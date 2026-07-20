# noCRM.io: List Lead Comments

Retrieves lead comments from noCRM.io.

```
GET https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-lead-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a noCRM.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-lead-comments?connectionId=$CONNECTION_ID&leadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-lead-comments?${params}`, {
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
| `leadId` | string | yes | Lead ID. |
| `direction` | string | no | Sort direction for returned comments. Default: `desc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentedItem": {
        "id": 1,
        "item": "string"
      },
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isPinned": true,
      "rawContent": "string",
      "user": {
        "email": "ava@example.com",
        "firstname": "Ava",
        "id": 1,
        "lastname": "Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentedItem.id` | number |  |
| `commentedItem.item` | string |  |
| `content` | string |  |
| `createdAt` | date |  |
| `id` | number |  |
| `isPinned` | boolean |  |
| `rawContent` | string |  |
| `user.email` | string |  |
| `user.firstname` | string |  |
| `user.id` | number |  |
| `user.lastname` | string |  |

## Native endpoint

Through the native noCRM.io API, this operation is `GET /leads/:lead_id/comments` (base URL `{{credentials.baseUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lead-comments.md) for the provider-specific parameters and requirements.

