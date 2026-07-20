# EchtPost Postcards: Delete Card

Deletes a saved postcard from EchtPost Postcards.

```
DELETE https://connect.mindcloud.co/v1/universal/echtPostPostcards/latest/actions/delete-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EchtPost Postcards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/echtPostPostcards/latest/actions/delete-card?connectionId=$CONNECTION_ID&cardId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cardId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/echtPostPostcards/latest/actions/delete-card?${params}`, {
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
| `cardId` | string | yes | The EchtPost card ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EchtPost Postcards API returns.

## Native endpoint

Through the native EchtPost Postcards API, this operation is `DELETE /cards/:id` (base URL `https://api.echtpost.de/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-card.md) for the provider-specific parameters and requirements.

