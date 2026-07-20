# e-Boekhouden.nl: Create Ledger

Creates a new ledger in e-Boekhouden.nl.

```
POST https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/create-ledger
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Boekhouden.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/create-ledger" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "code": "string",
  "description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/create-ledger', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "code": "string",
    "description": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `code` | string | yes | The code of the ledger. Error codes LEDG_001 Code is missing. LEDG_002 Code is too long. |
| `description` | string | yes | The description of the ledger. Error codes LEDG_003 Description is missing. LEDG_004 Description is too long. |
| `category` | string | no | A list of ledger categories is displayed below. Only these values may be used in `POST` and `PATCH` operations: `["BAL", "VW", "FIN", "DEB", "CRED"]`. \| Value \| Description \| \|---\|---\| \| BAL \| Balance \| \| VW \| Profit and loss \| \| AF6 \| Turnover tax low rate \| \| AF19 \| Turnover tax high rate \| \| AFOVERIG \| Turnover tax other \| \| VOOR \| Input tax \| \| BTWRC \| VAT current account \| \| FIN \| Liquid Assets \| \| DEB \| Debtors \| \| CRED \| Creditors \| \| AF \| Turnover tax \| |
| `group` | string | no | The group of the ledger. Error codes LEDG_007 Group is missing. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native e-Boekhouden.nl API returns.

## Native endpoint

Through the native e-Boekhouden.nl API, this operation is `POST /v1/ledger` (base URL `https://api.e-boekhouden.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ledger.md) for the provider-specific parameters and requirements.

