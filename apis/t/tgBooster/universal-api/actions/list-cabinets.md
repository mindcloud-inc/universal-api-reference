# TgBooster: List Cabinets

Retrieves Telegram Ads cabinets from TgBooster.

```
GET https://connect.mindcloud.co/v1/universal/tgBooster/latest/actions/list-cabinets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TgBooster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tgBooster/latest/actions/list-cabinets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tgBooster/latest/actions/list-cabinets?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "photo": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Cabinet creation timestamp. |
| `id` | number | Cabinet ID. |
| `name` | string | Cabinet name. |
| `photo` | string | Cabinet photo value. |

## Native endpoint

Through the native TgBooster API, this operation is `POST /cabinets` (base URL `https://api.tgbooster.ru/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cabinets.md) for the provider-specific parameters and requirements.

