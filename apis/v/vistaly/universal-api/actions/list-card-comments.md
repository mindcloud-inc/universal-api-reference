# Vistaly: List Card Comments

Retrieves comments for a card from Vistaly.

```
GET https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/list-card-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vistaly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/list-card-comments?connectionId=$CONNECTION_ID&cardId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cardId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/list-card-comments?${params}`, {
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
| `cardId` | string | yes | The unique identifier for the card. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vistaly API returns.

## Native endpoint

Through the native Vistaly API, this operation is `GET /beta/cards/{cardId}/comments` (base URL `https://api.vistaly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-card-comments.md) for the provider-specific parameters and requirements.

