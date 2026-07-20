# OneDesk: Get Customer By External ID

Retrieves a customer by external ID from OneDesk.

```
GET https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/get-customer-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/get-customer-by-external-id?connectionId=$CONNECTION_ID&externalId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "externalId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/get-customer-by-external-id?${params}`, {
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
| `externalId` | string | yes | External ID of the customer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "address1": {},
        "address2": {},
        "city": {},
        "country": {},
        "state": {},
        "zip": {}
      },
      "created": "2026-05-07T12:00:00.000Z",
      "customerOrganization": "string",
      "customerType": "string",
      "externalId": "string",
      "id": 1,
      "priority": 1,
      "profile": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "language": {},
        "lastName": "Chen",
        "phoneWork": {},
        "title": {}
      },
      "registered": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.address1` | object |  |
| `address.address2` | object |  |
| `address.city` | object |  |
| `address.country` | object |  |
| `address.state` | object |  |
| `address.zip` | object |  |
| `created` | date |  |
| `customerOrganization` | string |  |
| `customerType` | string |  |
| `externalId` | string |  |
| `id` | number |  |
| `priority` | number |  |
| `profile.email` | string |  |
| `profile.firstName` | string |  |
| `profile.language` | object |  |
| `profile.lastName` | string |  |
| `profile.phoneWork` | object |  |
| `profile.title` | object |  |
| `registered` | boolean |  |

## Native endpoint

Through the native OneDesk API, this operation is `GET /rest/public/customers/externalId/:externalId` (base URL `https://app.onedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-by-external-id.md) for the provider-specific parameters and requirements.

