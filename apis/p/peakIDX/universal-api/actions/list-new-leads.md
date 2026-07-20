# PeakIDX: List New Leads

Retrieves new leads from PeakIDX since the last sync.

```
GET https://connect.mindcloud.co/v1/universal/peakIDX/latest/actions/list-new-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PeakIDX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peakIDX/latest/actions/list-new-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peakIDX/latest/actions/list-new-leads?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leadType` | string | no | Optional comma-separated PeakIDX lead type names, such as Inquiry or Property Inquiry. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "allFields": "string",
          "comments": "string",
          "date": "string",
          "email": "ava@example.com",
          "firstName": "Ava",
          "id": "string",
          "lastName": "Chen",
          "leadType": "string",
          "listingId": "string",
          "phone": "string",
          "phone2": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[]` | array<object> | New PeakIDX leads returned since the last sync check. |
| `[].allFields` | string | Full multi-line text block returned by PeakIDX for the lead. |
| `[].comments` | string | Lead comments. |
| `[].date` | string | Lead timestamp returned by PeakIDX. |
| `[].email` | string | Lead email address. |
| `[].firstName` | string | Lead first name. |
| `[].id` | string | PeakIDX lead identifier from the new-leads feed. |
| `[].lastName` | string | Lead last name. |
| `[].leadType` | string | Lead type such as Inquiry or Property Inquiry. |
| `[].listingId` | string | Associated listing identifier when present. |
| `[].phone` | string | Primary lead phone number. |
| `[].phone2` | string | Secondary lead phone number when present. |

## Native endpoint

Through the native PeakIDX API, this operation is `GET https://account.peakidxsites.com/lead-api/new-leads` (base URL `https://account.peakidxsites.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-new-leads.md) for the provider-specific parameters and requirements.

