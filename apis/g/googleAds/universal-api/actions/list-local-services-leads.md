# Google Ads: List Local Services Leads

Retrieves local services leads from Google Ads.

```
GET https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-local-services-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-local-services-leads?connectionId=$CONNECTION_ID&customerId=1234567890&query=SELECT%20local_services_lead.id%20FROM%20local_services_lead%20LIMIT%2050" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1234567890",
  "query": "SELECT local_services_lead.id FROM local_services_lead LIMIT 50"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-local-services-leads?${params}`, {
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
| `customerId` | list | yes | Customer ID that owns the Google Ads resources (without dashes). Example: `1234567890`. |
| `query` | string | yes | GAQL query to list local services leads. Default: `SELECT local_services_lead.id, local_services_lead.category_id, local_services_lead.lead_status, local_services_lead.creation_date_time FROM local_services_lead ORDER BY local_services_lead.creation_date_time DESC LIMIT 50`. Example: `SELECT local_services_lead.id FROM local_services_lead LIMIT 50`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "localServicesLead": {
        "categoryId": "string",
        "creationDateTime": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "leadStatus": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `localServicesLead.categoryId` | string |  |
| `localServicesLead.creationDateTime` | date |  |
| `localServicesLead.id` | string |  |
| `localServicesLead.leadStatus` | string |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/googleAds:search` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-local-services-leads.md) for the provider-specific parameters and requirements.

