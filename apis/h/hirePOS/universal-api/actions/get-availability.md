# HirePOS: Get Availability

Retrieves item availability from HirePOS for a date range.

```
GET https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/get-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HirePOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/get-availability?connectionId=$CONNECTION_ID&dateFrom=2026-05-07T12%3A00%3A00.000Z&dateTo=2026-05-07T12%3A00%3A00.000Z&items%5B%5D=%5Bobject%20Object%5D&items%5B%5D.websiteCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dateFrom": "2026-05-07T12:00:00.000Z",
  "dateTo": "2026-05-07T12:00:00.000Z",
  "items[]": "[object Object]",
  "items[].websiteCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/get-availability?${params}`, {
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
| `dateFrom` | date | yes | Start of the requested availability window. |
| `dateTo` | date | yes | End of the requested availability window. |
| `items[]` | array<object> | yes | Array of website-code items to check for availability. |
| `items[].websiteCode` | string | yes | Website code for one item in the availability request. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `branchId` | number | no | Optional branch ID for accounts using the Branches module. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HirePOS API returns.

## Native endpoint

Through the native HirePOS API, this operation is `GET /Availability` (base URL `https://api.hirepos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-availability.md) for the provider-specific parameters and requirements.

