# Rakuten Advertising: List contributed conversions

Retrieves contributed conversions from Rakuten Advertising.

```
GET https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/list-contributed-conversions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rakuten Advertising `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/list-contributed-conversions?connectionId=$CONNECTION_ID&endDate=2026-05-07T12%3A00%3A00.000Z&startDate=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endDate": "2026-05-07T12:00:00.000Z",
  "startDate": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/list-contributed-conversions?${params}`, {
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
| `endDate` | date | yes | End date of conversion transaction date range in YYYY-MM-DD format. |
| `limit` | number | no | Number of records per page. Defaults to 1000. Default: `1000`. |
| `orderBy` | string | no | Sort order: asc or desc. |
| `page` | number | no | Page number. Defaults to 1. Default: `1`. |
| `sortBy` | string | no | Column to sort the contributed conversions by. Defaults to order date. |
| `startDate` | date | yes | Start date of conversion transaction date range in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "advertiserId": "string",
      "conversionPublisherCategory": "string",
      "journeyPosition": "string",
      "orderDatetime": "2026-05-07T12:00:00.000Z",
      "orderId": "string",
      "publisherId": "string",
      "u1": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `advertiserId` | string |  |
| `conversionPublisherCategory` | string |  |
| `journeyPosition` | string |  |
| `orderDatetime` | date |  |
| `orderId` | string |  |
| `publisherId` | string |  |
| `u1` | string |  |

## Native endpoint

Through the native Rakuten Advertising API, this operation is `GET /v1/publishers/contributed-conversions` (base URL `https://api.linksynergy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contributed-conversions.md) for the provider-specific parameters and requirements.

