# Octanist: Get Ad Spend

Retrieves ad spend data from Octanist.

```
GET https://connect.mindcloud.co/v1/universal/octanist/latest/actions/get-ad-spend
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Octanist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/octanist/latest/actions/get-ad-spend?connectionId=$CONNECTION_ID&startDate=2026-03-01&endDate=2026-03-25" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "2026-03-01",
  "endDate": "2026-03-25"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/octanist/latest/actions/get-ad-spend?${params}`, {
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
| `startDate` | string | yes | Start date in YYYY-MM-DD format. Example: `2026-03-01`. |
| `endDate` | string | yes | End date in YYYY-MM-DD format. Example: `2026-03-25`. |
| `platform` | string | no | Filter ad spend by platform. Example: `googleads`. |
| `groupBy` | string | no | Dimension to group ad spend by. Default: `date`. |
| `limit` | number | no | Results per page. Default: `100`. |
| `page` | number | no | Page number. Default: `1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Octanist API returns.

## Native endpoint

Through the native Octanist API, this operation is `POST /ad-spend` (base URL `https://octanist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ad-spend.md) for the provider-specific parameters and requirements.

