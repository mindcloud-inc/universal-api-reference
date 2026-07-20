# Favro: Delete Card

Deletes an existing card from Favro.

```
DELETE https://connect.mindcloud.co/v1/universal/favro/latest/actions/delete-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Favro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/favro/latest/actions/delete-card?connectionId=$CONNECTION_ID&cardId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cardId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/favro/latest/actions/delete-card?${params}`, {
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
| `cardId` | string | yes | The card ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cardId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cardId` | string |  |

## Native endpoint

Through the native Favro API, this operation is `DELETE /cards/:cardId` (base URL `https://favro.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-card.md) for the provider-specific parameters and requirements.

