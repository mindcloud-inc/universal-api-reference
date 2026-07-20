# FreeAgent: List Estimates

Retrieves a list of estimates from FreeAgent.

```
GET https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/list-estimates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreeAgent `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/list-estimates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/list-estimates?${params}`, {
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
| `contact` | string | no | Filter estimates by FreeAgent contact resource URL. |
| `invoice` | string | no | Filter estimates by FreeAgent invoice resource URL. |
| `project` | string | no | Filter estimates by FreeAgent project resource URL. |
| `updatedSince` | date | no | Only return estimates updated after this timestamp. |
| `view` | string | no | Filter the estimate collection by FreeAgent view. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": "string",
      "contact_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "dated_on": "2026-05-07T12:00:00.000Z",
      "estimate_type": "string",
      "include_sales_tax_on_total_value": true,
      "involves_sales_tax": true,
      "net_value": "string",
      "notes": "string",
      "project": "string",
      "reference": "string",
      "status": "string",
      "total_value": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | string |  |
| `contact_name` | string |  |
| `created_at` | date |  |
| `currency` | string |  |
| `dated_on` | date |  |
| `estimate_type` | string |  |
| `include_sales_tax_on_total_value` | boolean |  |
| `involves_sales_tax` | boolean |  |
| `net_value` | string |  |
| `notes` | string |  |
| `project` | string |  |
| `reference` | string |  |
| `status` | string |  |
| `total_value` | string |  |
| `updated_at` | date |  |
| `url` | string |  |

## Native endpoint

Through the native FreeAgent API, this operation is `GET /estimates` (base URL `https://api.freeagent.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-estimates.md) for the provider-specific parameters and requirements.

