# Twenty: List Companies



```
GET https://connect.mindcloud.co/v1/universal/twenty/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twenty/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twenty/latest/actions/list-companies?${params}`, {
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

Through the native Twenty API, this operation is `GET /rest/companies` (base URL `https://api.twenty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

