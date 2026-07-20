# mittwald: Get Customer Membership

Retrieves customer membership from mittwald API.

```
GET https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/get-customer-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mittwald `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/get-customer-membership?connectionId=$CONNECTION_ID&customerMembershipId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerMembershipId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/get-customer-membership?${params}`, {
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
| `customerMembershipId` | string | yes | Customer Membership ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerId": "string",
      "email": "ava@example.com",
      "id": "string",
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerId` | string |  |
| `email` | string |  |
| `id` | string |  |
| `role` | string |  |

## Native endpoint

Through the native mittwald API, this operation is `GET /v2/customer-memberships/:customerMembershipId` (base URL `https://api.mittwald.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-membership.md) for the provider-specific parameters and requirements.

