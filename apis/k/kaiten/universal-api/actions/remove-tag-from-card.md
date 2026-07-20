# Kaiten: Remove Tag from Card

Removes a tag from a Kaiten card.

```
DELETE https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/remove-tag-from-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kaiten `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/remove-tag-from-card?connectionId=$CONNECTION_ID&cardId=1&tagId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cardId": "1",
  "tagId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/remove-tag-from-card?${params}`, {
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
| `tagId` | number | yes | The Kaiten tag ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native Kaiten API, this operation is `DELETE /cards/:cardId/tags/:tagId` (base URL `https://{{credentials.companyDomain}}.kaiten.ru/api/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-tag-from-card.md) for the provider-specific parameters and requirements.

