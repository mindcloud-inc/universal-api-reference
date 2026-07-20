# Visma eAccounting: Create Article

Creates a new article in Visma eAccounting.

```
POST https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/create-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Visma eAccounting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/create-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/create-article', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "changedUtc": "2026-05-07T12:00:00.000Z",
      "createdUtc": "2026-05-07T12:00:00.000Z",
      "grossPrice": 1,
      "id": "string",
      "isActive": true,
      "name": "Ava Chen",
      "netPrice": 1,
      "number": "string",
      "stockBalance": 1,
      "unitName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changedUtc` | date |  |
| `createdUtc` | date |  |
| `grossPrice` | number |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `name` | string |  |
| `netPrice` | number |  |
| `number` | string |  |
| `stockBalance` | number |  |
| `unitName` | string |  |

## Native endpoint

Through the native Visma eAccounting API, this operation is `POST /articles` (base URL `https://eaccountingapi.vismaonline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-article.md) for the provider-specific parameters and requirements.

