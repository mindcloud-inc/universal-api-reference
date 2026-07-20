# e-Boekhouden.nl: Update Ledger

Updates a ledger in e-Boekhouden.nl.

```
PUT https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/update-ledger
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Boekhouden.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/update-ledger" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/update-ledger', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `code` | string | no | The code of the ledger. Error codes LEDG_001 Code is missing. LEDG_002 Code is too long. |
| `description` | string | no | The description of the ledger. Error codes LEDG_003 Description is missing. LEDG_004 Description is too long. |
| `category` | string | no | A list of ledger categories is displayed below. Only these values may be used in `POST` and `PATCH` operations: `["BAL", "VW", "FIN", "DEB", "CRED"]`. \| Value \| Description \| \|---\|---\| \| BAL \| Balance \| \| VW \| Profit and loss \| \| AF6 \| Turnover tax low rate \| \| AF19 \| Turnover tax high rate \| \| AFOVERIG \| Turnover tax other \| \| VOOR \| Input tax \| \| BTWRC \| VAT current account \| \| FIN \| Liquid Assets \| \| DEB \| Debtors \| \| CRED \| Creditors \| \| AF \| Turnover tax \| |
| `group` | string | no | The group of the ledger. Error codes LEDG_007 Group is missing. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native e-Boekhouden.nl API returns.

## Native endpoint

Through the native e-Boekhouden.nl API, this operation is `PATCH /v1/ledger/:id` (base URL `https://api.e-boekhouden.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ledger.md) for the provider-specific parameters and requirements.

