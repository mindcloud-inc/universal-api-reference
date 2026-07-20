# Supernotes: Get Comments

Retrieves comments for a Supernotes card.

```
GET https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supernotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-comments?connectionId=$CONNECTION_ID&cardId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cardId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-comments?${params}`, {
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
| `cardId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cardId": "string",
      "createdWhen": "2026-05-07T12:00:00.000Z",
      "html": "string",
      "id": "string",
      "markup": "string",
      "modifiedWhen": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cardId` | string |  |
| `createdWhen` | date |  |
| `html` | string |  |
| `id` | string |  |
| `markup` | string |  |
| `modifiedWhen` | date |  |
| `userId` | string |  |

## Native endpoint

Through the native Supernotes API, this operation is `GET /comments/:card_id` (base URL `https://api.supernotes.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-comments.md) for the provider-specific parameters and requirements.

