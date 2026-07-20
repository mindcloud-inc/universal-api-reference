# Fiserv: Create Fee

Creates a fee for a merchant account in Fiserv.

```
POST https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/create-fee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiserv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/create-fee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "xAccountId": "string",
  "feeType": "0",
  "amount": 1,
  "description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/create-fee', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "xAccountId": "string",
    "feeType": "0",
    "amount": 1,
    "description": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `xAccountId` | string | yes | Merchant account ID required in the x-account-id header. |
| `feeType` | list | yes | Fee type to create. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `amount` | number | yes | Fee amount in minor units. |
| `currency` | list | no | Currency for the fee. One of: `0`, `1`. |
| `description` | string | yes | Fee description. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `referenceId` | string | no | Optional external reference ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fiserv API returns.

## Native endpoint

Through the native Fiserv API, this operation is `POST /fees` (base URL `https://bankinghub-cert.fiservapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-fee.md) for the provider-specific parameters and requirements.

