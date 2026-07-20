# 1Shot: List Delegations

Retrieves delegations for a wallet in 1Shot API.

```
GET https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-delegations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1Shot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-delegations?connectionId=$CONNECTION_ID&walletId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "walletId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-delegations?${params}`, {
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
| `walletId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessId": "string",
      "contractAddresses": [
        "string"
      ],
      "created": 1,
      "delegationData": "string",
      "delegatorAddress": "string",
      "endTime": 1,
      "id": "string",
      "methods": [
        "string"
      ],
      "startTime": 1,
      "updated": 1,
      "walletId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessId` | string |  |
| `contractAddresses[]` | string |  |
| `created` | number |  |
| `delegationData` | string |  |
| `delegatorAddress` | string |  |
| `endTime` | number |  |
| `id` | string |  |
| `methods[]` | string |  |
| `startTime` | number |  |
| `updated` | number |  |
| `walletId` | string |  |

## Native endpoint

Through the native 1Shot API, this operation is `GET /wallets/:walletId/delegations` (base URL `https://api.1shotapi.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-delegations.md) for the provider-specific parameters and requirements.

