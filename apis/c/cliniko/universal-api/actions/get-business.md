# Cliniko: Get Business

Retrieves a business from your Cliniko account.

```
GET https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/get-business
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cliniko `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/get-business?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/get-business?${params}`, {
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
| `id` | string | yes | The Cliniko business ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalInformation": {},
      "additionalInvoiceInformation": {},
      "address1": {},
      "address2": {},
      "appointmentRemindersEnabled": true,
      "appointments": {
        "links": {
          "self": "https://example.com"
        }
      },
      "appointmentTypeIds": [
        "string"
      ],
      "archivedAt": {},
      "businessName": "Ava Chen",
      "businessRegistrationName": {},
      "businessRegistrationValue": {},
      "city": {},
      "contactInformation": {},
      "country": "string",
      "countryCode": "string",
      "createdAt": "string",
      "deletedAt": {},
      "displayName": {},
      "emailReplyTo": {},
      "id": "string",
      "label": "string",
      "links": {
        "self": "https://example.com"
      },
      "postCode": {},
      "practitioners": {
        "links": {
          "self": "https://example.com"
        }
      },
      "showInOnlineBookings": true,
      "state": {},
      "timeZone": "string",
      "timeZoneIdentifier": "string",
      "updatedAt": "string",
      "websiteAddress": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalInformation` | object |  |
| `additionalInvoiceInformation` | object |  |
| `address1` | object |  |
| `address2` | object |  |
| `appointmentRemindersEnabled` | boolean |  |
| `appointments.links.self` | string |  |
| `appointmentTypeIds[]` | string |  |
| `archivedAt` | object |  |
| `businessName` | string |  |
| `businessRegistrationName` | object |  |
| `businessRegistrationValue` | object |  |
| `city` | object |  |
| `contactInformation` | object |  |
| `country` | string |  |
| `countryCode` | string |  |
| `createdAt` | string |  |
| `deletedAt` | object |  |
| `displayName` | object |  |
| `emailReplyTo` | object |  |
| `id` | string |  |
| `label` | string |  |
| `links.self` | string |  |
| `postCode` | object |  |
| `practitioners.links.self` | string |  |
| `showInOnlineBookings` | boolean |  |
| `state` | object |  |
| `timeZone` | string |  |
| `timeZoneIdentifier` | string |  |
| `updatedAt` | string |  |
| `websiteAddress` | object |  |

## Native endpoint

Through the native Cliniko API, this operation is `GET /businesses/:id` (base URL `https://api.au5.cliniko.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-business.md) for the provider-specific parameters and requirements.

