# KeyVox: List Locks

Lists locks in your KeyVox account.

```
GET https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-locks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-locks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-locks?${params}`, {
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
| `page` | number | no | 1ページ目から指定 |
| `count` | number | no | 表示件数（最大100前後） |

## Response

```json
{
  "success": true,
  "data": [
    {
      "list": [
        {
          "lockId": "string",
          "lockName": "Ava Chen",
          "moduleId": "string",
          "moduleName": "Ava Chen"
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
| `list[].lockId` | string | スマートロックを識別するユニークIDです |
| `list[].lockName` | string | ロック表示名 |
| `list[].moduleId` | string | ロックのモデルと対応するコード |
| `list[].moduleName` | string | ロックのモデル |

## Native endpoint

Through the native KeyVox API, this operation is `POST /v1/getLocks` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-locks.md) for the provider-specific parameters and requirements.

