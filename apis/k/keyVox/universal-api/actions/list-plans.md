# KeyVox: List Plans

Lists room plans in your KeyVox account.

```
GET https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-plans?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "list": [
        {
          "commodityId": "string",
          "commodityName": "Ava Chen",
          "orgId": "string",
          "placeId": "string"
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
| `list[].commodityId` | string | 部屋プランID |
| `list[].commodityName` | string | 部屋プラン名 |
| `list[].orgId` | string | 組織ID |
| `list[].placeId` | string | 場所ID |

## Native endpoint

Through the native KeyVox API, this operation is `POST /plan/list` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-plans.md) for the provider-specific parameters and requirements.

