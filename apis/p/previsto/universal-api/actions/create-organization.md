# Previsto: Create Organization

Creates a new organization in Previsto.

```
POST https://connect.mindcloud.co/v1/universal/previsto/latest/actions/create-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Previsto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/previsto/latest/actions/create-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "location": "string",
  "name": "Ava Chen",
  "languageCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/previsto/latest/actions/create-organization', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "location": "string",
    "name": "Ava Chen",
    "languageCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | no | Street address |
| `city` | string | no | City |
| `countryCode` | string | no | 2-letter country code |
| `location` | string | yes | Location as [longitude, latitude]. Required by the live API. |
| `name` | string | yes | Organization name. |
| `postalCode` | string | no | Postal code |
| `languageCode` | string | yes | Organization language code. |
| `baseCurrency` | string | no | Organization base currency. |
| `timeZone` | string | no | Organization time zone. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "apiVersion": {},
      "appartment": {},
      "baseCurrency": "string",
      "city": "string",
      "countryCode": "string",
      "createdBy": "string",
      "createdDate": "string",
      "email": {},
      "id": "string",
      "languageCode": "string",
      "lastModifiedBy": "string",
      "lastModifiedDate": "string",
      "location": [
        1
      ],
      "name": "Ava Chen",
      "phone": {},
      "postalCode": "string",
      "registrationNo": {},
      "timeZone": "string",
      "url": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `apiVersion` | object |  |
| `appartment` | object |  |
| `baseCurrency` | string |  |
| `city` | string |  |
| `countryCode` | string |  |
| `createdBy` | string |  |
| `createdDate` | string |  |
| `email` | object |  |
| `id` | string |  |
| `languageCode` | string |  |
| `lastModifiedBy` | string |  |
| `lastModifiedDate` | string |  |
| `location[]` | number |  |
| `name` | string |  |
| `phone` | object |  |
| `postalCode` | string |  |
| `registrationNo` | object |  |
| `timeZone` | string |  |
| `url` | object |  |

## Native endpoint

Through the native Previsto API, this operation is `POST /organizations` (base URL `https://api.previsto.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-organization.md) for the provider-specific parameters and requirements.

