# Rakuten Advertising: Run advanced report

Retrieves an advanced report from Rakuten Advertising.

```
GET https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/run-advanced-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rakuten Advertising `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/run-advanced-report?connectionId=$CONNECTION_ID&bdate=string&edate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bdate": "string",
  "edate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/run-advanced-report?${params}`, {
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
| `bdate` | string | yes | Report begin date in YYYYMMDD format. |
| `edate` | string | yes | Report end date in YYYYMMDD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "advertiserId": "string",
      "advertiserName": "Ava Chen",
      "clicks": 1,
      "commissions": 1,
      "orders": 1,
      "rawRow": {},
      "reportId": "string",
      "rowId": "string",
      "sales": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `advertiserId` | string |  |
| `advertiserName` | string |  |
| `clicks` | number |  |
| `commissions` | number |  |
| `orders` | number |  |
| `rawRow` | object |  |
| `reportId` | string |  |
| `rowId` | string |  |
| `sales` | number |  |

## Native endpoint

Through the native Rakuten Advertising API, this operation is `GET /advancedreports/1.0` (base URL `https://api.linksynergy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-advanced-report.md) for the provider-specific parameters and requirements.

