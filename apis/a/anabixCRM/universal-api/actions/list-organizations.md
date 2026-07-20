# Anabix CRM: List Organizations

Retrieves organization records from Anabix CRM.

```
GET https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anabix CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/list-organizations?${params}`, {
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

Through the native Anabix CRM API, this operation is `POST /api` (base URL `https://app.anabix.cz`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

