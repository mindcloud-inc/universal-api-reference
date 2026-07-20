# Trello: Remove Label from Card

Removes a label from a Trello card.

```
DELETE https://connect.mindcloud.co/v1/universal/trello/latest/actions/remove-label-from-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trello `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/trello/latest/actions/remove-label-from-card?connectionId=$CONNECTION_ID&id=string&idLabel=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "idLabel": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trello/latest/actions/remove-label-from-card?${params}`, {
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
| `id` | string | yes | Card identifier. |
| `idLabel` | string | yes | Label identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object | Null value returned after the label is removed from the card. |

## Native endpoint

Through the native Trello API, this operation is `DELETE cards/:id/idLabels/:idLabel` (base URL `https://api.trello.com/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-label-from-card.md) for the provider-specific parameters and requirements.

