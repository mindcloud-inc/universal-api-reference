# PeakIDX: Create Or Update Lead

Creates or updates a lead in PeakIDX.

```
POST https://connect.mindcloud.co/v1/universal/peakIDX/latest/actions/create-or-update-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PeakIDX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/peakIDX/latest/actions/create-or-update-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/peakIDX/latest/actions/create-or-update-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leadId` | string | no | Unique identifier for the lead. |
| `leadType` | string | no | Lead category such as Inquiry, Property Inquiry, CMA Inquiry, or Mortgage Quote. |
| `leadFirstName` | string | no | Lead given name. |
| `leadLastName` | string | no | Lead family name. |
| `leadEmail` | string | no | Primary lead email address. |
| `leadPhone` | string | no | Primary lead phone number. |
| `leadComments` | string | no | Additional notes or context for the lead. |
| `leadListingId` | string | no | Associated listing identifier such as an MLS number. |
| `leadPhone2` | string | no | Secondary lead phone number. |
| `leadCreatedDatetime` | string | no | Lead creation timestamp in PeakIDX format such as 2024-03-22 12:00:00. |
| `leadCustomFields` | string | no | Multi-line custom field text formatted as Label: Value pairs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether PeakIDX accepted the lead upsert request. |

## Native endpoint

Through the native PeakIDX API, this operation is `POST https://account.peakidxsites.com/lead-api/create-lead` (base URL `https://account.peakidxsites.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-lead.md) for the provider-specific parameters and requirements.

