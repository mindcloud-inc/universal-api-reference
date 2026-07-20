# Paycove: Get Organization Details

Retrieves an organization from Paycove.

```
GET https://connect.mindcloud.co/v1/universal/paycove/latest/actions/get-organization-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/get-organization-details?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paycove/latest/actions/get-organization-details?${params}`, {
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
| `id` | string | yes | Paycove CRMOrganization ID. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "city": {},
      "country": {},
      "createdAt": "string",
      "creatorId": {},
      "crm": {},
      "crmOrganizationId": "string",
      "email": {},
      "facebook": {},
      "id": 1,
      "industry": {},
      "line1": {},
      "linkedin": {},
      "name": "Ava Chen",
      "ownerId": {},
      "phone": {},
      "postalCode": {},
      "state": {},
      "twitter": {},
      "updatedAt": "string",
      "website": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `city` | object |  |
| `country` | object |  |
| `createdAt` | string |  |
| `creatorId` | object |  |
| `crm` | object |  |
| `crmOrganizationId` | string |  |
| `email` | object |  |
| `facebook` | object |  |
| `id` | number |  |
| `industry` | object |  |
| `line1` | object |  |
| `linkedin` | object |  |
| `name` | string |  |
| `ownerId` | object |  |
| `phone` | object |  |
| `postalCode` | object |  |
| `state` | object |  |
| `twitter` | object |  |
| `updatedAt` | string |  |
| `website` | object |  |

## Native endpoint

Through the native Paycove API, this operation is `GET organizations/:id` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-details.md) for the provider-specific parameters and requirements.

