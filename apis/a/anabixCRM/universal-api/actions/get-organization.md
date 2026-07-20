# Anabix CRM: Get Organization

Retrieves an organization from Anabix CRM.

```
GET https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anabix CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/get-organization?connectionId=$CONNECTION_ID&data.idOrganization=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data.idOrganization": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/get-organization?${params}`, {
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
| `data.idOrganization` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountType": "string",
      "billingCity": "string",
      "billingCode": "string",
      "billingCountry": "string",
      "billingStreet": "string",
      "body": "string",
      "contacts": [
        {}
      ],
      "customFields": [
        {}
      ],
      "email": "ava@example.com",
      "email2": "ava@example.com",
      "email3": "ava@example.com",
      "emailDomain": "ava@example.com",
      "idNumber": "string",
      "idOrganization": 1,
      "invoices": [
        {}
      ],
      "phoneNumber": "string",
      "phoneNumber2": "string",
      "phoneNumber3": "string",
      "shippingCity": "string",
      "shippingCode": "string",
      "shippingCountry": "string",
      "shippingStreet": "string",
      "title": "Ava Chen",
      "vatNumber": "string",
      "website": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountType` | string |  |
| `billingCity` | string |  |
| `billingCode` | string |  |
| `billingCountry` | string |  |
| `billingStreet` | string |  |
| `body` | string |  |
| `contacts` | array<object> |  |
| `customFields` | array<object> |  |
| `email` | string |  |
| `email2` | string |  |
| `email3` | string |  |
| `emailDomain` | string |  |
| `idNumber` | string |  |
| `idOrganization` | number | Anabix organization ID. |
| `invoices` | array<object> |  |
| `phoneNumber` | string |  |
| `phoneNumber2` | string |  |
| `phoneNumber3` | string |  |
| `shippingCity` | string |  |
| `shippingCode` | string |  |
| `shippingCountry` | string |  |
| `shippingStreet` | string |  |
| `title` | string | Organization title. |
| `vatNumber` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Anabix CRM API, this operation is `POST /api` (base URL `https://app.anabix.cz`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

