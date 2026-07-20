# QuickFile: List Bank Accounts



```
GET https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/list-bank-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/list-bank-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/list-bank-accounts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "bankId": 1,
      "bankType": "string",
      "isDefaultAccount": true,
      "isHidden": true,
      "logoPath": "string",
      "name": "Ava Chen",
      "nominalCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bankId` | number | QuickFile bank account identifier. |
| `bankType` | string | QuickFile bank account type. |
| `isDefaultAccount` | boolean | Whether this is the default bank account. |
| `isHidden` | boolean | Whether the bank account is hidden. |
| `logoPath` | string | Optional provider logo path. |
| `name` | string | Display name of the bank account. |
| `nominalCode` | number | Nominal ledger code for the bank account. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /bank/getaccounts` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bank-accounts.md) for the provider-specific parameters and requirements.

