# Kaiten: Add Comment

Creates a comment on a Kaiten card.

```
POST https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/add-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kaiten `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/add-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cardId": 1,
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/add-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cardId": 1,
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cardId` | number | yes | The Kaiten card ID. |
| `text` | string | yes | The comment text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author_id": 1,
      "card_id": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "deleted": true,
      "edited": true,
      "email_addresses_to": "ava@example.com",
      "id": 1,
      "internal": true,
      "notification_sent": true,
      "sd_description": true,
      "sd_external_recipients_cc": "string",
      "text": "string",
      "type": 1,
      "uid": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author_id` | number | Author user ID |
| `card_id` | number | Card ID |
| `created` | date | Create timestamp |
| `deleted` | boolean | Deleted flag |
| `edited` | boolean | Edited flag |
| `email_addresses_to` | string | Destination emails |
| `id` | number | Comment ID |
| `internal` | boolean | Internal flag |
| `notification_sent` | boolean | Notification sent flag |
| `sd_description` | boolean | Support desk description flag |
| `sd_external_recipients_cc` | string | CC recipients |
| `text` | string | Comment text |
| `type` | number | Comment type |
| `uid` | string | Comment UID |
| `updated` | date | Update timestamp |

## Native endpoint

Through the native Kaiten API, this operation is `POST /cards/:cardId/comments` (base URL `https://{{credentials.companyDomain}}.kaiten.ru/api/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-comment.md) for the provider-specific parameters and requirements.

