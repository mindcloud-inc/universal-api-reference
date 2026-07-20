# QuickFile: List Bank Account Balances



```
GET https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/list-bank-account-balances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/list-bank-account-balances?connectionId=$CONNECTION_ID&nominalCodes=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "nominalCodes": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/list-bank-account-balances?${params}`, {
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
| `nominalCodes` | number | yes | One or more QuickFile bank nominal codes to fetch balances for. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "nominalCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Current balance reported by QuickFile for the nominal code. |
| `nominalCode` | number | QuickFile bank nominal code. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /bank/getaccountbalances` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bank-account-balances.md) for the provider-specific parameters and requirements.

