# BigCommerce (B2B): Get Company



```
GET https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigCommerce (B2B) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/get-company?${params}`, {
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
| `companyStatus` | number | no |  |
| `limit` | number | no |  |
| `include` | string | no |  |
| `companyId` | string | no |  |
| `bcGroupId` | string | no |  |
| `bcOrderId` | number | no |  |
| `customerId` | number | no |  |
| `extraFieldFilterType` | string | no |  |
| `extraFields[]` | array | no |  |
| `isIncludeExtraFields` | string | no | Example: `0`. |
| `maxCreated` | number | no |  |
| `maxModified` | number | no |  |
| `minCreated` | number | no |  |
| `minModified` | number | no |  |
| `orderBy` | string | no |  |
| `orderId` | string | no |  |
| `q` | string | no |  |
| `sortBy` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": [
        {
          "addressLine1": "string",
          "addressLine2": "string",
          "bcGroupId": 1,
          "bcGroupName": "Ava Chen",
          "catalogId": 1,
          "catalogName": "Ava Chen",
          "city": "string",
          "companyEmail": "ava@example.com",
          "companyId": 1,
          "companyName": "Ava Chen",
          "companyPhone": "string",
          "companyStatus": 1,
          "country": "string",
          "createdAt": 1,
          "parentCompany": {
            "id": {},
            "name": "Ava Chen"
          },
          "state": "string",
          "updatedAt": 1,
          "uuid": "string",
          "zipCode": "string"
        }
      ],
      "meta": {
        "message": "string",
        "pagination": {
          "limit": 1,
          "offset": 1,
          "totalCount": 1
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
| `code` | number |  |
| `data[].addressLine1` | string |  |
| `data[].addressLine2` | string |  |
| `data[].bcGroupId` | number |  |
| `data[].bcGroupName` | string |  |
| `data[].catalogId` | number |  |
| `data[].catalogName` | string |  |
| `data[].city` | string |  |
| `data[].companyEmail` | string |  |
| `data[].companyId` | number |  |
| `data[].companyName` | string |  |
| `data[].companyPhone` | string |  |
| `data[].companyStatus` | number |  |
| `data[].country` | string |  |
| `data[].createdAt` | number |  |
| `data[].parentCompany.id` | object |  |
| `data[].parentCompany.name` | string |  |
| `data[].state` | string |  |
| `data[].updatedAt` | number |  |
| `data[].uuid` | string |  |
| `data[].zipCode` | string |  |
| `meta.message` | string |  |
| `meta.pagination.limit` | number |  |
| `meta.pagination.offset` | number |  |
| `meta.pagination.totalCount` | number |  |

## Native endpoint

Through the native BigCommerce (B2B) API, this operation is `GET companies/:companyId` (base URL `https://api-b2b.bigcommerce.com/api/v3/io/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

