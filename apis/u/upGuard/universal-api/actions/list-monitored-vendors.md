# UpGuard: List Monitored Vendors

Retrieves monitored vendors from your UpGuard portfolio.

```
GET https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-monitored-vendors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-monitored-vendors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-monitored-vendors?${params}`, {
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
| `includeAdHocReports` | boolean | no | Include vendors that already have an ad hoc report in the results. |
| `labels[]` | array<string> | no | Filter vendors by the provided labels. Accepts multiple values in one string, delimited by `,`. |
| `includeRisks` | boolean | no | Include risks in each vendor result. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "totalResults": 1,
      "vendors": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `totalResults` | number |  |
| `vendors` | object |  |

## Native endpoint

Through the native UpGuard API, this operation is `GET /vendors` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-monitored-vendors.md) for the provider-specific parameters and requirements.

