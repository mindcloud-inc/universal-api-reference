# Leadfeeder: Get Lead

Retrieves a specific lead from Leadfeeder.

```
GET https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/get-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadfeeder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/get-lead?connectionId=$CONNECTION_ID&leadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/get-lead?${params}`, {
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
| `leadId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "assignee": "string",
        "business_id": "string",
        "crm_lead_id": 1,
        "crm_organization_id": "string",
        "emailed_to": "ava@example.com",
        "employee_count": 1,
        "employees_range": {},
        "facebook_url": "https://example.com",
        "first_visit_date": "string",
        "industries": [
          {}
        ],
        "industry": "string",
        "last_visit_date": "string",
        "linkedin_url": "https://example.com",
        "logo_url": "https://example.com",
        "name": "Ava Chen",
        "phone": "string",
        "revenue": "string",
        "status": "string",
        "tags": [
          "string"
        ],
        "twitter_handle": "string",
        "view_in_leadfeeder": "string",
        "visits": 1,
        "website_url": "https://example.com"
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
| `attributes.assignee` | string |  |
| `attributes.business_id` | string |  |
| `attributes.crm_lead_id` | number |  |
| `attributes.crm_organization_id` | string |  |
| `attributes.emailed_to` | string |  |
| `attributes.employee_count` | number |  |
| `attributes.employees_range` | object |  |
| `attributes.facebook_url` | string |  |
| `attributes.first_visit_date` | string |  |
| `attributes.industries` | array<object> |  |
| `attributes.industry` | string |  |
| `attributes.last_visit_date` | string |  |
| `attributes.linkedin_url` | string |  |
| `attributes.logo_url` | string |  |
| `attributes.name` | string |  |
| `attributes.phone` | string |  |
| `attributes.revenue` | string |  |
| `attributes.status` | string |  |
| `attributes.tags` | array<string> |  |
| `attributes.twitter_handle` | string |  |
| `attributes.view_in_leadfeeder` | string |  |
| `attributes.visits` | number |  |
| `attributes.website_url` | string |  |
| `id` | string |  |
| `relationships.location.data.id` | string |  |
| `relationships.location.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Leadfeeder API, this operation is `GET /accounts/:accountId/leads/:leadId` (base URL `https://api.leadfeeder.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead.md) for the provider-specific parameters and requirements.

