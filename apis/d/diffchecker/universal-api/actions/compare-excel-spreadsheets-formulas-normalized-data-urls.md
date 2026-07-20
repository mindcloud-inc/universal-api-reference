# Diffchecker: Compare Excel Spreadsheets (Formulas, Normalized, Data URLs)

Compares Excel spreadsheets in Diffchecker using normalized formulas from data URLs.

```
GET https://connect.mindcloud.co/v1/universal/diffchecker/latest/actions/compare-excel-spreadsheets-formulas-normalized-data-urls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Diffchecker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diffchecker/latest/actions/compare-excel-spreadsheets-formulas-normalized-data-urls?connectionId=$CONNECTION_ID&leftSpreadsheet=string&rightSpreadsheet=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leftSpreadsheet": "string",
  "rightSpreadsheet": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diffchecker/latest/actions/compare-excel-spreadsheets-formulas-normalized-data-urls?${params}`, {
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
| `leftSpreadsheet` | string | yes | Left spreadsheet as a data URL. |
| `rightSpreadsheet` | string | yes | Right spreadsheet as a data URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columns": [
        {}
      ],
      "rows": [
        {}
      ],
      "stats": {},
      "table": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columns` | array<object> | Column-level diff metadata. |
| `rows` | array<object> | Row-level diff metadata. |
| `stats` | object | Summary statistics for the spreadsheet diff. |
| `table` | array<object> | Cell-level diff output grouped by rows. |

## Native endpoint

Through the native Diffchecker API, this operation is `POST /excel` (base URL `https://api.diffchecker.com/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compare-excel-spreadsheets-formulas-normalized-data-urls.md) for the provider-specific parameters and requirements.

