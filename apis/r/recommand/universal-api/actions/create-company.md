# Recommand: Create Company

Creates a new company in Recommand.

```
POST https://connect.mindcloud.co/v1/universal/recommand/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address": "string",
  "city": "string",
  "country": "string",
  "name": "Ava Chen",
  "postalcode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recommand/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address": "string",
    "city": "string",
    "country": "string",
    "name": "Ava Chen",
    "postalcode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | yes | address body field. |
| `city` | string | yes | city body field. |
| `country` | string | yes | country body field. |
| `email` | string | no | email body field. |
| `enterprisenumber` | string | no | The enterprise number of the company. Can only contain alphanumeric characters. For Belgian businesses it will be inferred from the VAT number if not provided. |
| `enterprisenumberscheme` | string | no | enterpriseNumberScheme body field. |
| `issmprecipient` | boolean | no | isSmpRecipient body field. |
| `name` | string | yes | name body field. |
| `phone` | string | no | phone body field. |
| `postalcode` | string | yes | postalCode body field. |
| `skipdefaultcompanysetup` | boolean | no | If true, the automatic creation of company identifiers and document types will be skipped. You will need to create them afterwards using the company identifier creation endpoint and company document type creation endpoint. |
| `vatnumber` | string | no | vatNumber body field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {
        "address": "string",
        "city": "string",
        "country": "string",
        "createdAt": "string",
        "email": "ava@example.com",
        "enterpriseNumber": "string",
        "enterpriseNumberScheme": "string",
        "id": "string",
        "isSmpRecipient": true,
        "isVerified": true,
        "name": "Ava Chen",
        "phone": "string",
        "postalCode": "string",
        "teamId": "string",
        "updatedAt": "string",
        "vatNumber": "string"
      },
      "success": true,
      "verificationUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object |  |
| `company.address` | string |  |
| `company.city` | string |  |
| `company.country` | string |  |
| `company.createdAt` | string |  |
| `company.email` | string |  |
| `company.enterpriseNumber` | string |  |
| `company.enterpriseNumberScheme` | string |  |
| `company.id` | string |  |
| `company.isSmpRecipient` | boolean |  |
| `company.isVerified` | boolean |  |
| `company.name` | string |  |
| `company.phone` | string |  |
| `company.postalCode` | string |  |
| `company.teamId` | string |  |
| `company.updatedAt` | string |  |
| `company.vatNumber` | string |  |
| `success` | boolean |  |
| `verificationUrl` | string |  |

## Native endpoint

Through the native Recommand API, this operation is `POST /api/v1/companies` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

