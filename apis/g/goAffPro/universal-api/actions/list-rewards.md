# GoAffPro: List Rewards

Retrieves a list of affiliate rewards from GoAffPro.

```
GET https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-rewards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoAffPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-rewards?connectionId=$CONNECTION_ID&fields%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fields[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-rewards?${params}`, {
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
| `affiliateId` | string | no | Only return rewards for this affiliate ID. |
| `fields[]` | array<string> | yes | Fields to include in returned rewards. |
| `status` | string | no | Only return rewards with this status. |
| `type` | string | no | Only return rewards with this type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliateId": 1,
      "amount": 1,
      "created": "string",
      "id": 1,
      "level": 1,
      "metadata": "string",
      "orderId": 1,
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliateId` | number |  |
| `amount` | number |  |
| `created` | string |  |
| `id` | number |  |
| `level` | number |  |
| `metadata` | string |  |
| `orderId` | number |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native GoAffPro API, this operation is `GET /admin/rewards` (base URL `https://api.goaffpro.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-rewards.md) for the provider-specific parameters and requirements.

