# Nucleus One: Get Organization Permissions

Retrieves organization permissions from Nucleus One.

```
GET https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/get-organization-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nucleus One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/get-organization-permissions?connectionId=$CONNECTION_ID&organizationId=Enter%20organizationId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "Enter organizationId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/get-organization-permissions?${params}`, {
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
| `organizationId` | string | yes | ID of the organization Example: `Enter organizationId`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$schema": "string",
      "Disabled": true,
      "IsAdmin": true,
      "IsReadOnly": true,
      "OrganizationID": "string",
      "OrganizationMemberID": "string",
      "OrganizationName": "Ava Chen",
      "UserEmail": "ava@example.com",
      "UserID": "string",
      "UserName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$schema` | string |  |
| `Disabled` | boolean |  |
| `IsAdmin` | boolean |  |
| `IsReadOnly` | boolean |  |
| `OrganizationID` | string |  |
| `OrganizationMemberID` | string |  |
| `OrganizationName` | string |  |
| `UserEmail` | string |  |
| `UserID` | string |  |
| `UserName` | string |  |

## Native endpoint

Through the native Nucleus One API, this operation is `GET /organizations/:organizationId/permissions` (base URL `https://client-api.nucleus.one/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-permissions.md) for the provider-specific parameters and requirements.

