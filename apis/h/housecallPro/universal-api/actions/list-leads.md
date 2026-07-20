# Housecall Pro: List Leads



```
GET https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/list-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Housecall Pro `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/list-leads?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/list-leads?${params}`, {
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
| `customerId` | string | no | Filters leads by a single customer ID (string) |
| `status` | list | no | Filters leads by status One of: `lost`, `open`, `won`. |
| `leadSource[]` | array<string> | no | Filters leads by a single lead_source |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `employeeIds[]` | array<string> | no | Filters leads by a list of employee IDs (string) |
| `tagIds[]` | array<string> | no | Filters leads by a list of tags |
| `locationIds[]` | array<string> | no | IDs of locations to pull from. Ignored when X-Company-Id is set. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "assignedEmployee": {},
      "companyId": "string",
      "companyName": "Ava Chen",
      "conversions": [
        {}
      ],
      "customer": {},
      "id": "string",
      "leadSource": "string",
      "lostAt": "2026-05-07T12:00:00.000Z",
      "number": 1,
      "pipelineStatus": "string",
      "status": "string",
      "tags": [
        "string"
      ],
      "totalAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object | Lead address details. |
| `assignedEmployee` | object | Assigned employee. |
| `companyId` | string | Company ID. |
| `companyName` | string | Company name. |
| `conversions` | array<object> | Lead conversions. |
| `customer` | object | Customer attached to the lead. |
| `id` | string | Lead ID. |
| `leadSource` | string | Lead source. |
| `lostAt` | date | Timestamp when the lead was marked lost. |
| `number` | number | Lead number. |
| `pipelineStatus` | string | Pipeline status. |
| `status` | string | Lead status. |
| `tags` | array<string> | Lead tags. |
| `totalAmount` | number | Lead total amount. |

## Native endpoint

Through the native Housecall Pro API, this operation is `GET /leads` (base URL `https://api.housecallpro.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-leads.md) for the provider-specific parameters and requirements.

