# ProProfs Project: Get Company

Retrieves company details from ProProfs Project.

```
GET https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/get-company?${params}`, {
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
      "address1": "string",
      "address2": "string",
      "autoIds": "string",
      "billingEmail": "ava@example.com",
      "city": "string",
      "companyId": "string",
      "companyName": "Ava Chen",
      "country": "string",
      "currency": "string",
      "customCss": "string",
      "customHeaderBg": "string",
      "dateCreated": "string",
      "dateOrder": "string",
      "defaultOrder": "string",
      "domain": "string",
      "estimateEmailTemplate": "ava@example.com",
      "estimateFooter": "string",
      "firstDay": "string",
      "invoiceEmailTemplate": "ava@example.com",
      "invoiceFooter": "string",
      "language": "string",
      "logo": "string",
      "phone": "string",
      "postcode": "string",
      "progressType": "string",
      "roundBillableHours": "string",
      "signature": "string",
      "state": "string",
      "superuserId": "string",
      "timezone": "string",
      "users": [
        {
          "userId": "string",
          "userName": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address1` | string |  |
| `address2` | string |  |
| `autoIds` | string |  |
| `billingEmail` | string |  |
| `city` | string |  |
| `companyId` | string |  |
| `companyName` | string |  |
| `country` | string |  |
| `currency` | string |  |
| `customCss` | string |  |
| `customHeaderBg` | string |  |
| `dateCreated` | string |  |
| `dateOrder` | string |  |
| `defaultOrder` | string |  |
| `domain` | string |  |
| `estimateEmailTemplate` | string |  |
| `estimateFooter` | string |  |
| `firstDay` | string |  |
| `invoiceEmailTemplate` | string |  |
| `invoiceFooter` | string |  |
| `language` | string |  |
| `logo` | string |  |
| `phone` | string |  |
| `postcode` | string |  |
| `progressType` | string |  |
| `roundBillableHours` | string |  |
| `signature` | string |  |
| `state` | string |  |
| `superuserId` | string |  |
| `timezone` | string |  |
| `users[].userId` | string |  |
| `users[].userName` | string |  |

## Native endpoint

Through the native ProProfs Project API, this operation is `GET /company` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

