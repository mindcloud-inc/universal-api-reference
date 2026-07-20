# Twenty: Create Company



```
POST https://connect.mindcloud.co/v1/universal/twenty/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/twenty/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idealCustomerProfile": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/twenty/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "idealCustomerProfile": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domainName.primaryLinkLabel` | string | no |  |
| `domainName.primaryLinkUrl` | string | no |  |
| `domainName.secondaryLinks[]` | array<string> | no |  |
| `name` | string | no |  |
| `xLink.primaryLinkLabel` | string | no |  |
| `xLink.primaryLinkUrl` | string | no |  |
| `xLink.secondaryLinks[]` | array<string> | no |  |
| `employees` | number | no |  |
| `idealCustomerProfile` | boolean | yes |  |
| `address.addressStreet1` | string | no |  |
| `address.addressStreet2` | string | no |  |
| `address.addressCity` | string | no |  |
| `address.addressPostcode` | string | no |  |
| `address.addressState` | string | no |  |
| `address.addressCountry` | string | no |  |
| `linkedinLink.primaryLinkLabel` | string | no |  |
| `linkedinLink.primaryLinkUrl` | string | no |  |
| `linkedinLink.secondaryLinks[]` | array<string> | no |  |
| `accountOwnerId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountOwnerId": "string",
      "address": {
        "addressCity": "string",
        "addressCountry": "string",
        "addressPostcode": "string",
        "addressState": "string",
        "addressStreet1": "string",
        "addressStreet2": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {
        "name": "Ava Chen",
        "source": "string"
      },
      "deletedAt": "string",
      "domainName": {
        "primaryLinkLabel": "https://example.com",
        "primaryLinkUrl": "https://example.com",
        "secondaryLinks": [
          "https://example.com"
        ]
      },
      "employees": 1,
      "id": "string",
      "idealCustomerProfile": true,
      "linkedinLink": {
        "primaryLinkLabel": "https://example.com",
        "primaryLinkUrl": "https://example.com",
        "secondaryLinks": [
          "https://example.com"
        ]
      },
      "name": "Ava Chen",
      "position": 1,
      "searchVector": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": {
        "name": "Ava Chen",
        "source": "string"
      },
      "xLink": {
        "primaryLinkLabel": "https://example.com",
        "primaryLinkUrl": "https://example.com",
        "secondaryLinks": [
          "https://example.com"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountOwnerId` | string |  |
| `address.addressCity` | string |  |
| `address.addressCountry` | string |  |
| `address.addressPostcode` | string |  |
| `address.addressState` | string |  |
| `address.addressStreet1` | string |  |
| `address.addressStreet2` | string |  |
| `createdAt` | date |  |
| `createdBy.name` | string |  |
| `createdBy.source` | string |  |
| `deletedAt` | string |  |
| `domainName.primaryLinkLabel` | string |  |
| `domainName.primaryLinkUrl` | string |  |
| `domainName.secondaryLinks` | array<string> |  |
| `employees` | number |  |
| `id` | string |  |
| `idealCustomerProfile` | boolean |  |
| `linkedinLink.primaryLinkLabel` | string |  |
| `linkedinLink.primaryLinkUrl` | string |  |
| `linkedinLink.secondaryLinks` | array<string> |  |
| `name` | string |  |
| `position` | number |  |
| `searchVector` | string |  |
| `updatedAt` | date |  |
| `updatedBy.name` | string |  |
| `updatedBy.source` | string |  |
| `xLink.primaryLinkLabel` | string |  |
| `xLink.primaryLinkUrl` | string |  |
| `xLink.secondaryLinks` | array<string> |  |

## Native endpoint

Through the native Twenty API, this operation is `POST /rest/companies` (base URL `https://api.twenty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

