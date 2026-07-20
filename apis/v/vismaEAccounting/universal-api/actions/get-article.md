# Visma eAccounting: Get Article

Retrieves an article from Visma eAccounting.

```
GET https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/get-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Visma eAccounting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/get-article?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/get-article?${params}`, {
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

Through the native Visma eAccounting API, this operation is `GET /articles/{articleId}` (base URL `https://eaccountingapi.vismaonline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-article.md) for the provider-specific parameters and requirements.

