# Kaiten: Retrieve List of Card Tags

Retrieves tags for a Kaiten card.

```
GET https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-list-of-card-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kaiten `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-list-of-card-tags?connectionId=$CONNECTION_ID&cardId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cardId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-list-of-card-tags?${params}`, {
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
      "archived": true,
      "color": 1,
      "company_id": 1,
      "created": "string",
      "id": 1,
      "locked": true,
      "name": "Ava Chen",
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
| `archived` | boolean |  |
| `color` | number |  |
| `company_id` | number |  |
| `created` | string |  |
| `id` | number |  |
| `locked` | boolean |  |
| `name` | string |  |
| `uid` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native Kaiten API, this operation is `GET /cards/:cardId/tags` (base URL `https://{{credentials.companyDomain}}.kaiten.ru/api/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-list-of-card-tags.md) for the provider-specific parameters and requirements.

