# Previsto: Update Organization

Updates an existing organization in Previsto.

```
PUT https://connect.mindcloud.co/v1/universal/previsto/latest/actions/update-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Previsto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/previsto/latest/actions/update-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/previsto/latest/actions/update-organization', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Previsto organization ID. |
| `name` | string | no | Updated organization name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "apiVersion": "string",
      "appartment": {},
      "baseCurrency": "string",
      "city": "string",
      "countryCode": "string",
      "createdBy": "string",
      "createdDate": "string",
      "email": "ava@example.com",
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
      "taxRates": [
        {
          "rate": 1,
          "workType": "string"
        }
      ],
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
| `apiVersion` | string |  |
| `appartment` | object |  |
| `baseCurrency` | string |  |
| `city` | string |  |
| `countryCode` | string |  |
| `createdBy` | string |  |
| `createdDate` | string |  |
| `email` | string |  |
| `id` | string |  |
| `languageCode` | string |  |
| `lastModifiedBy` | string |  |
| `lastModifiedDate` | string |  |
| `location[]` | number |  |
| `name` | string |  |
| `phone` | object |  |
| `postalCode` | string |  |
| `registrationNo` | object |  |
| `taxRates[].rate` | number |  |
| `taxRates[].workType` | string |  |
| `timeZone` | string |  |
| `url` | object |  |

## Native endpoint

Through the native Previsto API, this operation is `PUT /organizations/:id` (base URL `https://api.previsto.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-organization.md) for the provider-specific parameters and requirements.

