# 1Shot: Create Delegation

Creates a new wallet delegation in 1Shot API.

```
POST https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/create-delegation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1Shot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/create-delegation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "walletId": "string",
  "delegationData": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/create-delegation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "walletId": "string",
    "delegationData": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `walletId` | string | yes |  |
| `delegationData` | list<string> | yes | Live provider runtime currently requires delegationData as an array-shaped body value, even though the published OpenAPI documents a single JSON string. Each array element should be one serialized delegation payload string. |
| `startTime` | date | no |  |
| `endTime` | date | no |  |
| `contractAddresses` | list<string> | no |  |
| `methods` | list<string> | no |  |

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

Through the native 1Shot API, this operation is `POST /wallets/:walletId/delegations` (base URL `https://api.1shotapi.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-delegation.md) for the provider-specific parameters and requirements.

