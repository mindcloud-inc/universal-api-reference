# KeyVox: List Unit PINs

Lists unit PINs in your KeyVox account.

```
GET https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-unit-pi-ns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-unit-pi-ns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-unit-pi-ns?${params}`, {
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
      "pinList": [
        {
          "id": "string",
          "pinId": "string"
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
| `pinList[].id` | string | 返却された暗証番号情報に割り当てられる連番となります |
| `pinList[].pinId` | string | 暗証番号を識別するユニークIDです |
| `position` | string | 取得レコードの位置を示すポインタIDです |
| `records` | string | 取得レコード数 |

## Native endpoint

Through the native KeyVox API, this operation is `POST /v1/getUnitPinList` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-unit-pi-ns.md) for the provider-specific parameters and requirements.

