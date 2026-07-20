# Kaiten: Retrieve Card Comments

Retrieves comments for a Kaiten card.

```
GET https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-card-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kaiten `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-card-comments?connectionId=$CONNECTION_ID&cardId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cardId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-card-comments?${params}`, {
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
| `cardId` | number | yes | The Kaiten card ID. |

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
      "id": 1,
      "internal": true,
      "sd_description": true,
      "text": "string",
      "type": 1,
      "uid": "string",
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
| `id` | number |  |
| `internal` | boolean |  |
| `sd_description` | boolean |  |
| `text` | string |  |
| `type` | number |  |
| `uid` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native Kaiten API, this operation is `GET /cards/:cardId/comments` (base URL `https://{{credentials.companyDomain}}.kaiten.ru/api/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-card-comments.md) for the provider-specific parameters and requirements.

