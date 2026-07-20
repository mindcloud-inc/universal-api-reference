# Nucleus One: Get Organization Membership Package

Retrieves organization membership details from Nucleus One.

```
GET https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/get-organization-membership-package
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nucleus One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/get-organization-membership-package?connectionId=$CONNECTION_ID&organizationId=Enter%20organizationId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "Enter organizationId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/get-organization-membership-package?${params}`, {
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
      "Expiration": "2026-05-07T12:00:00.000Z",
      "FreeUsers": 1,
      "IsAdmin": true,
      "IsExpired": true,
      "IsExpiringSoon": true,
      "Organization": {},
      "OrganizationMember": {},
      "UserID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$schema` | string |  |
| `Expiration` | date |  |
| `FreeUsers` | number |  |
| `IsAdmin` | boolean |  |
| `IsExpired` | boolean |  |
| `IsExpiringSoon` | boolean |  |
| `Organization` | object |  |
| `OrganizationMember` | object |  |
| `UserID` | string |  |

## Native endpoint

Through the native Nucleus One API, this operation is `GET /organizationMembershipPackages/:organizationId` (base URL `https://client-api.nucleus.one/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-membership-package.md) for the provider-specific parameters and requirements.

