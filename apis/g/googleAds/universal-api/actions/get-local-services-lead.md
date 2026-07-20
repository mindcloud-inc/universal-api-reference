# Google Ads: Get Local Services Lead

Retrieves a local services lead from Google Ads.

```
GET https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/get-local-services-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/get-local-services-lead?connectionId=$CONNECTION_ID&customerId=1234567890&query=SELECT%20local_services_lead.id%20FROM%20local_services_lead%20WHERE%20local_services_lead.resource_name%20%3D%20'customers%2F1234567890%2FlocalServicesLeads%2FLEAD_ID'%20LIMIT%201" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1234567890",
  "query": "SELECT local_services_lead.id FROM local_services_lead WHERE local_services_lead.resource_name = 'customers/1234567890/localServicesLeads/LEAD_ID' LIMIT 1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/get-local-services-lead?${params}`, {
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
| `query` | string | yes | GAQL query to retrieve a specific local services lead. Default: `SELECT local_services_lead.id, local_services_lead.lead_status, local_services_lead.creation_date_time FROM local_services_lead WHERE local_services_lead.resource_name = 'customers/1234567890/localServicesLeads/LEAD_ID' LIMIT 1`. Example: `SELECT local_services_lead.id FROM local_services_lead WHERE local_services_lead.resource_name = 'customers/1234567890/localServicesLeads/LEAD_ID' LIMIT 1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leadId` | string | no | Optional local services lead ID for convenience when composing a query. Example: `LEAD_ID`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fieldMask": "string",
      "queryResourceConsumption": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fieldMask` | string |  |
| `queryResourceConsumption` | string |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/googleAds:search` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-local-services-lead.md) for the provider-specific parameters and requirements.

