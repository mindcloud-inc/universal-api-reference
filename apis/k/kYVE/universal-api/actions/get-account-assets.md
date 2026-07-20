# KYVE: Get Account Assets



```
GET https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-account-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KYVE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-account-assets?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-account-assets?${params}`, {
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
| `address` | string | yes | KYVE account address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": "string",
      "commission_rewards": [
        {}
      ],
      "delegation": "string",
      "delegation_rewards": [
        {}
      ],
      "delegation_unbonding": "string",
      "protocol_funding": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | string |  |
| `commission_rewards` | array<object> |  |
| `delegation` | string |  |
| `delegation_rewards` | array<object> |  |
| `delegation_unbonding` | string |  |
| `protocol_funding` | array<object> |  |

## Native endpoint

Through the native KYVE API, this operation is `GET /kyve/query/v1beta1/account_assets/{address}` (base URL `https://api.kyve.network`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-assets.md) for the provider-specific parameters and requirements.

