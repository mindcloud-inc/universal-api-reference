# KeyVox: List Reservable Units

Lists doors in your KeyVox account.

```
GET https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-reservable-units
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-reservable-units?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-reservable-units?${params}`, {
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
| `count` | string | no | １ページ件数 |
| `page` | string | no | ページ番号 |
| `placeId` | string | no | 場所ID |
| `searchWord` | string | no | 検索キーワード |
| `unitBusinessType` | string | no | ビジネスタイプ<br>"housing":宿泊, "rentalSpace":レンタルスペース, "conferenceRoom":コーワーキング, "locker":ロッカー, "airdrop":ドロップイン, "vendingMachine":自動販売機 |

## Response

```json
{
  "success": true,
  "data": [
    {
      "list": [
        {
          "orgId": "string",
          "placeAddress": "string",
          "placeId": "string",
          "placeName": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `list[].orgId` | string | 組織ID |
| `list[].placeAddress` | string | 住所 |
| `list[].placeId` | string | 場所ID |
| `list[].placeName` | string | 場所名 |

## Native endpoint

Through the native KeyVox API, this operation is `POST /unit/list` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reservable-units.md) for the provider-specific parameters and requirements.

