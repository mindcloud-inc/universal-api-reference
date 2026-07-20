# Recommand: Get Company

Retrieves a company record from Recommand.

```
GET https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-company?connectionId=$CONNECTION_ID&companyid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recommand/latest/actions/get-company?${params}`, {
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
| `companyid` | string | yes | companyId parameter. |

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

Through the native Recommand API, this operation is `GET /api/v1/companies/:companyId` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

