# BambooHR: Get Member Benefits

Retrieves member benefit enrollments from BambooHR.

```
GET https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/get-member-benefits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BambooHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/get-member-benefits?connectionId=$CONNECTION_ID&calendarYear=2026" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "calendarYear": "2026"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/get-member-benefits?${params}`, {
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
| `calendarYear` | string | yes | Calendar year to return benefit membership for. Example: `2026`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BambooHR API returns.

## Native endpoint

Through the native BambooHR API, this operation is `GET /v1/benefits/member-benefits` (base URL `https://mindcloud.bamboohr.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-member-benefits.md) for the provider-specific parameters and requirements.

