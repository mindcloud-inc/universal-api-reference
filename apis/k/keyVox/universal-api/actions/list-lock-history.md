# KeyVox: List Lock History

Lists lock history in your KeyVox account.

```
GET https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-lock-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-lock-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-lock-history?${params}`, {
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
      "history": [
        {
          "etime": "string",
          "etype": "string"
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
| `history[].etime` | string | 利用終了日時です。1970/01/01からの秒数(UNIX時間)で指定します |
| `history[].etype` | string | 鍵の種類です。<br> 1:PIN(暗証番号), 2:Card(NFCカード), 5:OPEN/CLOSE Button(スマートロックのボタン), 6:Knob Button(サムターン), 9:Application(including API)(アプリなどのサービス) |
| `position` | string | 取得レコードの位置を示すポインタIDです |
| `records` | string | 取得レコード数 |

## Native endpoint

Through the native KeyVox API, this operation is `POST /v1/getLockHistory` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lock-history.md) for the provider-specific parameters and requirements.

