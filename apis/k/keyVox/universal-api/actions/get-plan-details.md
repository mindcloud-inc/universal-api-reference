# KeyVox: Get Plan Details

Retrieves room plan details from KeyVox.

```
GET https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/get-plan-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/get-plan-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/get-plan-details?${params}`, {
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
| `commodityId` | string | no | 部屋プランID |
| `placeId` | string | no | 場所ID |
| `targetType` | string | no | プランタイプ<br>"order":予約<br>"order"で指定された場合、「貸出不可時間」を返却する |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commodityId": "string",
      "commodityName": "Ava Chen",
      "orgId": "string",
      "placeId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commodityId` | string | 部屋プランID |
| `commodityName` | string | 部屋プラン名 |
| `orgId` | string | 組織ID |
| `placeId` | string | 場所ID |

## Native endpoint

Through the native KeyVox API, this operation is `POST /plan/detail` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-plan-details.md) for the provider-specific parameters and requirements.

