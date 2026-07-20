# QuickFile: Get Chart Of Accounts



```
GET https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-chart-of-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-chart-of-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-chart-of-accounts?${params}`, {
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
| `startNominalCode` | number | no | Starting nominal code for the chart of accounts range. Default: `1`. |
| `endNominalCode` | number | no | Ending nominal code for the chart of accounts range. Default: `9999`. |
| `fromDate` | date | no | Optional lower bound date for nominal balances. |
| `toDate` | date | no | Optional upper bound date for nominal balances. |
| `excludeZeroBalanceLedgers` | boolean | no | When true, omits ledgers with a zero balance in the selected range. Defaults to false so the full chart of accounts is returned. Default: `false`. |
| `returnCodeName` | boolean | no | When true, includes the nominal code name. Default: `true`. |
| `returnDescription` | boolean | no | When true, includes the nominal code description. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "description": "string",
      "name": "Ava Chen",
      "nominalCode": 1,
      "systemCode": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Current balance for the nominal ledger in the selected date range. |
| `description` | string | Nominal ledger description. |
| `name` | string | Nominal ledger name. |
| `nominalCode` | number | QuickFile nominal ledger code. |
| `systemCode` | boolean | Whether the nominal ledger is a built-in QuickFile system code. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /report/chartofaccounts` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chart-of-accounts.md) for the provider-specific parameters and requirements.

