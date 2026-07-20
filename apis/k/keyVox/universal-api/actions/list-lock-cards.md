# KeyVox: List Lock Cards

Lists lock cards in your KeyVox account.

```
GET https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-lock-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-lock-cards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-lock-cards?${params}`, {
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
      "cardList": [
        {
          "cardId": "string",
          "id": "string"
        }
      ],
      "position": "string",
      "records": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cardList[].cardId` | string | カードを識別するユニークIDです |
| `cardList[].id` | string | id |
| `position` | string | 取得レコードが全体で何番目かの位置を示す情報です |
| `records` | string | 取得レコード数 |

## Native endpoint

Through the native KeyVox API, this operation is `POST /v1/getLockCardList` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lock-cards.md) for the provider-specific parameters and requirements.

