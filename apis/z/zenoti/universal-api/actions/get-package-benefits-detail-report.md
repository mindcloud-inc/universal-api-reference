# Zenoti: Get Package Benefits Detail Report



```
GET https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/get-package-benefits-detail-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenoti `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/get-package-benefits-detail-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/get-package-benefits-detail-report?${params}`, {
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
| `centers[]` | array | no |  |
| `centers[].center` | list | no |  |
| `dateType` | list | no |  |
| `startDate` | date | no |  |
| `endDate` | date | no | Don't set end date when the Date Type is "Balance As On Date" |
| `includeTotal` | boolean | no | Default: `True`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zenoti API returns.

## Native endpoint

Through the native Zenoti API, this operation is `POST reports/packages/benefits/flat_file` (base URL `https://api.zenoti.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-package-benefits-detail-report.md) for the provider-specific parameters and requirements.

