# Recommand: Update Company

Updates an existing company in Recommand.

```
PUT https://connect.mindcloud.co/v1/universal/recommand/latest/actions/update-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/update-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recommand/latest/actions/update-company', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | no | address body field. |
| `city` | string | no | city body field. |
| `companyid` | string | yes | companyId parameter. |
| `country` | string | no | country body field. |
| `email` | string | no | email body field. |
| `enterprisenumber` | string | no | enterpriseNumber body field. |
| `enterprisenumberscheme` | string | no | enterpriseNumberScheme body field. |
| `issmprecipient` | boolean | no | isSmpRecipient body field. |
| `name` | string | no | name body field. |
| `phone` | string | no | phone body field. |
| `postalcode` | string | no | postalCode body field. |
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
      "success": true
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

## Native endpoint

Through the native Recommand API, this operation is `PUT /api/v1/companies/:companyId` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company.md) for the provider-specific parameters and requirements.

