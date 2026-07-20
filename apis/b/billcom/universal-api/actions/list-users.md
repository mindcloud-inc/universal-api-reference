# BILL Payables & Receivables: List Users

Retrieves users from Bill.com.

```
GET https://connect.mindcloud.co/v1/universal/billcom/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BILL Payables & Receivables `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billcom/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billcom/latest/actions/list-users?${params}`, {
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
| `filters[]` | array | no |  |
| `filters[].field` | string | no |  |
| `filters[].comparison` | list | no |  |
| `filters[].value` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "string",
      "email": "ava@example.com",
      "entity": "string",
      "firstName": "Ava",
      "id": "string",
      "isActive": "string",
      "isVeridVerified": true,
      "lastName": "Chen",
      "loginId": "string",
      "organizationName": "Ava Chen",
      "orgId": "string",
      "partnerUserGroupType": "string",
      "profileId": "string",
      "timezoneId": "string",
      "updatedTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | string |  |
| `email` | string |  |
| `entity` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `isActive` | string |  |
| `isVeridVerified` | boolean |  |
| `lastName` | string |  |
| `loginId` | string |  |
| `organizationName` | string |  |
| `orgId` | string |  |
| `partnerUserGroupType` | string |  |
| `profileId` | string |  |
| `timezoneId` | string |  |
| `updatedTime` | string |  |

## Native endpoint

Through the native BILL Payables & Receivables API, this operation is `POST List/User.json` (base URL `https://api.bill.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

