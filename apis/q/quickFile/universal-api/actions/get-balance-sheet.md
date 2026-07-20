# QuickFile: Get Balance Sheet



```
GET https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-balance-sheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-balance-sheet?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-balance-sheet?${params}`, {
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
| `toDate` | date | no | Snapshot date for the balance sheet. |
| `showAsNbv` | boolean | no | When true, shows the balance sheet as net book value. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capitalAndReserves": 1,
      "currentAssets": 1,
      "currentLiabilities": 1,
      "fixedAssets": 1,
      "longTermLiabilities": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capitalAndReserves` | number | Balance sheet capital and reserves total. |
| `currentAssets` | number | Balance sheet current assets total. |
| `currentLiabilities` | number | Balance sheet current liabilities total. |
| `fixedAssets` | number | Balance sheet fixed assets total. |
| `longTermLiabilities` | number | Balance sheet long-term liabilities total. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /report/balancesheet` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-balance-sheet.md) for the provider-specific parameters and requirements.

