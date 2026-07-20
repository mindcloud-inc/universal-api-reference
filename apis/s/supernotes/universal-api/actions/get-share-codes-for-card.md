# Supernotes: Get Share Codes For Card

Retrieves share codes for a Supernotes card.

```
GET https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-share-codes-for-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supernotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-share-codes-for-card?connectionId=$CONNECTION_ID&cardId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cardId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-share-codes-for-card?${params}`, {
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
      "code": "string",
      "grantedPerms": 1,
      "id": "string",
      "ownerId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cardId` | string |  |
| `code` | string |  |
| `grantedPerms` | number |  |
| `id` | string |  |
| `ownerId` | string |  |

## Native endpoint

Through the native Supernotes API, this operation is `GET /sharing/:card_id` (base URL `https://api.supernotes.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-share-codes-for-card.md) for the provider-specific parameters and requirements.

