# Aspire: List Attachments



```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-attachments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-attachments?${params}`, {
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
| `$filter` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activityID": {},
      "activityNumber": {},
      "attachmentID": 1,
      "attachmentName": "Ava Chen",
      "attachmentTypeID": 1,
      "attachmentTypeName": "Ava Chen",
      "attachToInvoice": true,
      "contactID": {},
      "contactName": {},
      "dateUploaded": "string",
      "employeeIncidentID": {},
      "equipmentDescription": {},
      "equipmentID": {},
      "exposeToCrew": true,
      "externalContentID": {},
      "fileExtension": "string",
      "gEOLocationLatitude": {},
      "gEOLocationLongitude": {},
      "note": {},
      "notificationTemplateID": {},
      "opportunityID": 1,
      "opportunityNumber": 1,
      "originalFileName": "Ava Chen",
      "propertyID": 1,
      "propertyName": "Ava Chen",
      "propertyQACategoryID": {},
      "receiptID": {},
      "receiptNumber": {},
      "showCustomer": {},
      "workTicketID": {},
      "workTicketNumber": {},
      "workTicketVisitID": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activityID` | object |  |
| `activityNumber` | object |  |
| `attachmentID` | number |  |
| `attachmentName` | string |  |
| `attachmentTypeID` | number |  |
| `attachmentTypeName` | string |  |
| `attachToInvoice` | boolean |  |
| `contactID` | object |  |
| `contactName` | object |  |
| `dateUploaded` | string |  |
| `employeeIncidentID` | object |  |
| `equipmentDescription` | object |  |
| `equipmentID` | object |  |
| `exposeToCrew` | boolean |  |
| `externalContentID` | object |  |
| `fileExtension` | string |  |
| `gEOLocationLatitude` | object |  |
| `gEOLocationLongitude` | object |  |
| `note` | object |  |
| `notificationTemplateID` | object |  |
| `opportunityID` | number |  |
| `opportunityNumber` | number |  |
| `originalFileName` | string |  |
| `propertyID` | number |  |
| `propertyName` | string |  |
| `propertyQACategoryID` | object |  |
| `receiptID` | object |  |
| `receiptNumber` | object |  |
| `showCustomer` | object |  |
| `workTicketID` | object |  |
| `workTicketNumber` | object |  |
| `workTicketVisitID` | object |  |

## Native endpoint

Through the native Aspire API, this operation is `GET Attachments` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-attachments.md) for the provider-specific parameters and requirements.

