# Cinode: List Customers

Retrieves a company customer list from Cinode.

```
GET https://connect.mindcloud.co/v1/universal/cinode/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cinode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cinode/latest/actions/list-customers?connectionId=$CONNECTION_ID&companyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cinode/latest/actions/list-customers?${params}`, {
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
| `companyId` | number | yes | Cinode company ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": 1,
      "corporateIdentityNumber": "string",
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "email": "ava@example.com",
      "id": 1,
      "intermediator": true,
      "lastTouchDateTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "seoId": "string",
      "turnOver": 1,
      "updatedDateTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | number |  |
| `corporateIdentityNumber` | string |  |
| `createdDateTime` | date |  |
| `description` | string |  |
| `email` | string |  |
| `id` | number |  |
| `intermediator` | boolean |  |
| `lastTouchDateTime` | date |  |
| `name` | string |  |
| `seoId` | string |  |
| `turnOver` | number |  |
| `updatedDateTime` | date |  |

## Native endpoint

Through the native Cinode API, this operation is `GET /v0.1/companies/:companyId/customers` (base URL `https://api.cinode.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

