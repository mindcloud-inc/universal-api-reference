# Dealfront: Get Lead

Retrieves a lead from Dealfront.

```
GET https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/get-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dealfront `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/get-lead?connectionId=$CONNECTION_ID&accountId=1&leadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1",
  "leadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/get-lead?${params}`, {
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
| `accountId` | number | yes | ID of the account that owns the lead. |
| `leadId` | string | yes | ID of the lead to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "firstVisitDate": "2026-05-07T12:00:00.000Z",
        "industries": [
          {
            "name": "Ava Chen"
          }
        ],
        "industry": "string",
        "lastVisitDate": "2026-05-07T12:00:00.000Z",
        "linkedinUrl": "https://example.com",
        "logoUrl": "https://example.com",
        "name": "Ava Chen",
        "quality": 1,
        "status": "string",
        "viewInLeadfeeder": "string",
        "visits": 1,
        "websiteUrl": "https://example.com"
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
| `attributes.firstVisitDate` | date |  |
| `attributes.industries[].name` | string |  |
| `attributes.industry` | string |  |
| `attributes.lastVisitDate` | date |  |
| `attributes.linkedinUrl` | string |  |
| `attributes.logoUrl` | string |  |
| `attributes.name` | string |  |
| `attributes.quality` | number |  |
| `attributes.status` | string |  |
| `attributes.viewInLeadfeeder` | string |  |
| `attributes.visits` | number |  |
| `attributes.websiteUrl` | string |  |
| `id` | string |  |
| `relationships.location.data.id` | string |  |
| `relationships.location.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Dealfront API, this operation is `GET /accounts/:account_id/leads/:lead_id` (base URL `https://api.leadfeeder.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead.md) for the provider-specific parameters and requirements.

