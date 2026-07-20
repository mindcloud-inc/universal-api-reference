# Leadfeeder: Get Visits

Retrieves visits for an account in Leadfeeder by date range.

```
GET https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/get-visits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadfeeder `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/get-visits?connectionId=$CONNECTION_ID&limit=25&offset=0&startDate=2026-04-01&endDate=2026-04-13" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "startDate": "2026-04-01",
  "endDate": "2026-04-13"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/get-visits?${params}`, {
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
| `startDate` | date | yes | Example: `2026-04-01`. |
| `endDate` | date | yes | Example: `2026-04-13`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "adobe_cookies": [
          {}
        ],
        "campaign": "string",
        "country_code": "string",
        "date": "string",
        "device_type": "string",
        "hour": 1,
        "keyword": "string",
        "landing_page_path": "string",
        "lead_id": "string",
        "lf_client_id": 1,
        "medium": "string",
        "page_depth": 1,
        "query_term": "string",
        "referring_url": "https://example.com",
        "source": "string",
        "started_at": "string",
        "visit_length": 1,
        "visit_route": [
          {}
        ],
        "visitor_email": "ava@example.com",
        "visitor_first_name": "Ava",
        "visitor_last_name": "Chen"
      },
      "id": "string",
      "relationships": {
        "location": {
          "data": {
            "id": "string",
            "type": "string"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.adobe_cookies` | array<object> |  |
| `attributes.campaign` | string |  |
| `attributes.country_code` | string |  |
| `attributes.date` | string |  |
| `attributes.device_type` | string |  |
| `attributes.hour` | number |  |
| `attributes.keyword` | string |  |
| `attributes.landing_page_path` | string |  |
| `attributes.lead_id` | string |  |
| `attributes.lf_client_id` | number |  |
| `attributes.medium` | string |  |
| `attributes.page_depth` | number |  |
| `attributes.query_term` | string |  |
| `attributes.referring_url` | string |  |
| `attributes.source` | string |  |
| `attributes.started_at` | string |  |
| `attributes.visit_length` | number |  |
| `attributes.visit_route` | array<object> |  |
| `attributes.visitor_email` | string |  |
| `attributes.visitor_first_name` | string |  |
| `attributes.visitor_last_name` | string |  |
| `id` | string |  |
| `relationships.location.data.id` | string |  |
| `relationships.location.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Leadfeeder API, this operation is `GET /accounts/:accountId/visits` (base URL `https://api.leadfeeder.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-visits.md) for the provider-specific parameters and requirements.

