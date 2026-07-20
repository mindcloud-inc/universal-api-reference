# Kaiten: Update Comment

Updates an existing comment in Kaiten.

```
PUT https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/update-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kaiten `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/update-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cardId": 1,
  "commentId": 1,
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/update-comment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cardId": 1,
    "commentId": 1,
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
| `commentId` | number | yes | The Kaiten comment ID. |
| `text` | string | yes | The comment text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author_id": 1,
      "card_id": 1,
      "created": "string",
      "deleted": true,
      "edited": true,
      "email_addresses_to": "ava@example.com",
      "id": 1,
      "internal": true,
      "notification_sent": "string",
      "sd_description": true,
      "sd_external_recipients_cc": "string",
      "text": "string",
      "type": 1,
      "uid": 1,
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author_id` | number |  |
| `card_id` | number |  |
| `created` | string |  |
| `deleted` | boolean |  |
| `edited` | boolean |  |
| `email_addresses_to` | string |  |
| `id` | number |  |
| `internal` | boolean |  |
| `notification_sent` | string |  |
| `sd_description` | boolean |  |
| `sd_external_recipients_cc` | string |  |
| `text` | string |  |
| `type` | number |  |
| `uid` | number |  |
| `updated` | string |  |

## Native endpoint

Through the native Kaiten API, this operation is `PATCH /cards/:cardId/comments/:commentId` (base URL `https://{{credentials.companyDomain}}.kaiten.ru/api/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-comment.md) for the provider-specific parameters and requirements.

