# Nucleus One: List Project Membership Packages

Retrieves project memberships from a Nucleus One organization.

```
GET https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-project-membership-packages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nucleus One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-project-membership-packages?connectionId=$CONNECTION_ID&organizationId=Enter%20organizationId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "Enter organizationId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-project-membership-packages?${params}`, {
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
      "IsAdmin": true,
      "OrganizationID": "string",
      "OrganizationMemberID": "string",
      "Project": {},
      "ProjectMember": {},
      "UserID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `IsAdmin` | boolean |  |
| `OrganizationID` | string |  |
| `OrganizationMemberID` | string |  |
| `Project` | object |  |
| `ProjectMember` | object |  |
| `UserID` | string |  |

## Native endpoint

Through the native Nucleus One API, this operation is `GET /organizations/:organizationId/projectMembershipPackages` (base URL `https://client-api.nucleus.one/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-membership-packages.md) for the provider-specific parameters and requirements.

