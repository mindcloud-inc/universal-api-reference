# Mailtrap: Get Sending Stats by Categories

Retrieves Mailtrap sending stats by category.

```
GET https://connect.mindcloud.co/v1/universal/mailtrap/latest/actions/get-sending-stats-by-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailtrap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailtrap/latest/actions/get-sending-stats-by-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailtrap/latest/actions/get-sending-stats-by-categories?${params}`, {
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
      "bounceCount": 1,
      "bounceRate": 1,
      "category": "string",
      "clickCount": 1,
      "clickRate": 1,
      "deliveryCount": 1,
      "deliveryRate": 1,
      "openCount": 1,
      "openRate": 1,
      "spamCount": 1,
      "spamRate": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounceCount` | number |  |
| `bounceRate` | number |  |
| `category` | string |  |
| `clickCount` | number |  |
| `clickRate` | number |  |
| `deliveryCount` | number |  |
| `deliveryRate` | number |  |
| `openCount` | number |  |
| `openRate` | number |  |
| `spamCount` | number |  |
| `spamRate` | number |  |

## Native endpoint

Through the native Mailtrap API, this operation is `GET /stats/categories` (base URL `https://mailtrap.io/api/accounts/:account_id`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sending-stats-by-categories.md) for the provider-specific parameters and requirements.

