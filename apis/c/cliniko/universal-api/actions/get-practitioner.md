# Cliniko: Get Practitioner

Retrieves a practitioner from your Cliniko account.

```
GET https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/get-practitioner
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cliniko `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/get-practitioner?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/get-practitioner?${params}`, {
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
| `id` | string | yes | The Cliniko practitioner ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "appointments": {
        "links": {
          "self": "https://example.com"
        }
      },
      "appointmentTypes": {
        "links": {
          "self": "https://example.com"
        }
      },
      "createdAt": "string",
      "description": {},
      "designation": {},
      "displayName": "Ava Chen",
      "firstName": "Ava",
      "id": "string",
      "invoices": {
        "links": {
          "self": "https://example.com"
        }
      },
      "label": "string",
      "lastName": "Chen",
      "links": {
        "self": "https://example.com"
      },
      "practitionerReferenceNumbers": {
        "links": {
          "self": "https://example.com"
        }
      },
      "showInOnlineBookings": true,
      "title": {},
      "updatedAt": "string",
      "user": {
        "links": {
          "self": "https://example.com"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `appointments.links.self` | string |  |
| `appointmentTypes.links.self` | string |  |
| `createdAt` | string |  |
| `description` | object |  |
| `designation` | object |  |
| `displayName` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `invoices.links.self` | string |  |
| `label` | string |  |
| `lastName` | string |  |
| `links.self` | string |  |
| `practitionerReferenceNumbers.links.self` | string |  |
| `showInOnlineBookings` | boolean |  |
| `title` | object |  |
| `updatedAt` | string |  |
| `user.links.self` | string |  |

## Native endpoint

Through the native Cliniko API, this operation is `GET /practitioners/:id` (base URL `https://api.au5.cliniko.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-practitioner.md) for the provider-specific parameters and requirements.

