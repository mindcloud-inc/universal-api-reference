# Morningmate: List Employees v2

Retrieves employees from Morningmate's v2 API.

```
GET https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/list-employees-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morningmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/list-employees-v2?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/list-employees-v2?${params}`, {
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
| `cursor` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyPhoneNumber": "string",
      "divisionCode": "string",
      "divisionName": "Ava Chen",
      "email": "ava@example.com",
      "institutionId": "string",
      "isActive": true,
      "name": "Ava Chen",
      "phoneNumber": "string",
      "responsibility": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyPhoneNumber` | string | Company phone number. |
| `divisionCode` | string | Division code. |
| `divisionName` | string | Division name. |
| `email` | string | Email address. |
| `institutionId` | string | Institution identifier. |
| `isActive` | boolean | Whether the employee is active. |
| `name` | string | Display name. |
| `phoneNumber` | string | Phone number. |
| `responsibility` | string | Responsibility or role. |
| `userId` | string | Morningmate user identifier. |

## Native endpoint

Through the native Morningmate API, this operation is `GET /v2/employees` (base URL `https://api.morningmate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employees-v2.md) for the provider-specific parameters and requirements.

