# Keap: Update Company



```
PUT https://connect.mindcloud.co/v1/universal/keap/latest/actions/update-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/keap/latest/actions/update-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "company_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keap/latest/actions/update-company', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "company_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | no |  |
| `company_id` | string | yes | The unique identifier of the company. |
| `company_name` | string | no |  |
| `custom_fields` | string | no |  |
| `email_address` | string | no |  |
| `fax_number` | string | no |  |
| `notes` | string | no |  |
| `phone_number` | string | no |  |
| `update_mask` | string | no |  |
| `website` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "country": "string",
        "countryCode": "string",
        "field": "string",
        "line1": "string",
        "line2": "string",
        "locality": "string",
        "postalCode": "string",
        "region": "string",
        "regionCode": "string",
        "zipCode": "string",
        "zipFour": "string"
      },
      "companyName": "Ava Chen",
      "createTime": "string",
      "customFields": [
        {
          "content": "string",
          "id": "string"
        }
      ],
      "emailAddress": {
        "email": "ava@example.com",
        "emailOptStatus": "ava@example.com",
        "field": "ava@example.com",
        "isOptIn": "ava@example.com",
        "optInReason": "ava@example.com"
      },
      "faxNumber": {
        "field": "string",
        "number": "string",
        "type": "string"
      },
      "id": "string",
      "notes": "string",
      "phoneNumber": {
        "extension": "string",
        "field": "string",
        "number": "string",
        "numberE164": "string",
        "type": "string"
      },
      "updateTime": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.country` | string |  |
| `address.countryCode` | string |  |
| `address.field` | string |  |
| `address.line1` | string |  |
| `address.line2` | string |  |
| `address.locality` | string |  |
| `address.postalCode` | string |  |
| `address.region` | string |  |
| `address.regionCode` | string |  |
| `address.zipCode` | string |  |
| `address.zipFour` | string |  |
| `companyName` | string |  |
| `createTime` | string |  |
| `customFields[].content` | string |  |
| `customFields[].id` | string |  |
| `emailAddress.email` | string |  |
| `emailAddress.emailOptStatus` | string |  |
| `emailAddress.field` | string |  |
| `emailAddress.isOptIn` | string |  |
| `emailAddress.optInReason` | string |  |
| `faxNumber.field` | string |  |
| `faxNumber.number` | string |  |
| `faxNumber.type` | string |  |
| `id` | string |  |
| `notes` | string |  |
| `phoneNumber.extension` | string |  |
| `phoneNumber.field` | string |  |
| `phoneNumber.number` | string |  |
| `phoneNumber.numberE164` | string |  |
| `phoneNumber.type` | string |  |
| `updateTime` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Keap API, this operation is `PATCH /companies/{company_id}` (base URL `https://api.infusionsoft.com/crm/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company.md) for the provider-specific parameters and requirements.

