# Formitize: List Jobs

Retrieves jobs from Formitize.

```
GET https://connect.mindcloud.co/v1/universal/formitize/latest/actions/list-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formitize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formitize/latest/actions/list-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formitize/latest/actions/list-jobs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedTo": "string",
      "billingName": "Ava Chen",
      "clientID": "string",
      "contactID": "string",
      "contactName": "Ava Chen",
      "description": "string",
      "dueDate": "string",
      "duration": "string",
      "forms": {},
      "id": "string",
      "invoiceID": "string",
      "invoiceNumber": "string",
      "jobNumber": "string",
      "location": "string",
      "maintenanceID": "string",
      "orderNumber": "string",
      "priority": "string",
      "status": "string",
      "statusLabel": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedTo` | string |  |
| `billingName` | string |  |
| `clientID` | string |  |
| `contactID` | string |  |
| `contactName` | string |  |
| `description` | string |  |
| `dueDate` | string |  |
| `duration` | string |  |
| `forms` | object |  |
| `id` | string |  |
| `invoiceID` | string |  |
| `invoiceNumber` | string |  |
| `jobNumber` | string |  |
| `location` | string |  |
| `maintenanceID` | string |  |
| `orderNumber` | string |  |
| `priority` | string |  |
| `status` | string |  |
| `statusLabel` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Formitize API, this operation is `GET /job/` (base URL `https://service.formitize.com/api/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-jobs.md) for the provider-specific parameters and requirements.

