# Kaiten: Retrieve Board

Retrieves a board from Kaiten.

```
GET https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-board
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kaiten `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-board?connectionId=$CONNECTION_ID&spaceId=1&boardId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "1",
  "boardId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-board?${params}`, {
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
| `spaceId` | number | yes | The Kaiten space ID. |
| `boardId` | number | yes | The Kaiten board ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "board_id": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "default_card_type_id": 1,
      "description": "string",
      "email_key": "ava@example.com",
      "id": 1,
      "primary_path": true,
      "space_id": 1,
      "title": "string",
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
| `board_id` | number |  |
| `created` | date |  |
| `default_card_type_id` | number |  |
| `description` | string |  |
| `email_key` | string |  |
| `id` | number |  |
| `primary_path` | boolean |  |
| `space_id` | number |  |
| `title` | string |  |
| `uid` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Kaiten API, this operation is `GET /spaces/:spaceId/boards/:boardId` (base URL `https://{{credentials.companyDomain}}.kaiten.ru/api/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-board.md) for the provider-specific parameters and requirements.

