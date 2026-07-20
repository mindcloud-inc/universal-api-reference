# Amazon Seller: List Settlement Report List

Retrieves Settlement reports from Amazon Seller.

```
GET https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/list-settlement-report-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/list-settlement-report-list?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/list-settlement-report-list?${params}`, {
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
| `reportTypes` | list | no | One of: `GET_V2_SETTLEMENT_REPORT_DATA_FLAT_FILE_V2`. Accepts multiple values as an array. |
| `processingStatuses` | string | no | Accepts multiple values as an array. |
| `createdSince` | date | no |  |
| `createdUntil` | date | no |  |
| `nextToken` | string | no |  |
| `pageSize` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Amazon Seller API returns.

## Native endpoint

Through the native Amazon Seller API, this operation is `GET reports/2021-06-30/reports` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-settlement-report-list.md) for the provider-specific parameters and requirements.

