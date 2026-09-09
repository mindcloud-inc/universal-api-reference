# Walmart: Recon Report

Retrieves details of all orders with optional search criteria.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/recon-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/recon-report?connectionId=$CONNECTION_ID&limit=25&offset=0&reportDate=v1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "reportDate": "v1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/recon-report?${params}`, {
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
| `reportDate` | string | yes | Default: `v1`. Example: `v1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Walmart API returns.

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/report/reconreport/reconFileJson` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/recon-report.md) for the provider-specific parameters and requirements.

