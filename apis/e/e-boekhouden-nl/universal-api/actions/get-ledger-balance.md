# e-Boekhouden.nl: Get Ledger Balance

Retrieves a ledger balance from e-Boekhouden.nl.

```
GET https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/get-ledger-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Boekhouden.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/get-ledger-balance?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/get-ledger-balance?${params}`, {
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
| `costCenterId` | number | no | The ID of the cost center. |
| `from` | date | no | Show the balance starting from this date. When provided, the resulting balance is the difference over the period, rather than the actual balance. |
| `to` | date | no | Shows the active balance at this date. This date is inclusive. |
| `id` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native e-Boekhouden.nl API returns.

## Native endpoint

Through the native e-Boekhouden.nl API, this operation is `GET /v1/ledger/:id/balance` (base URL `https://api.e-boekhouden.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ledger-balance.md) for the provider-specific parameters and requirements.

