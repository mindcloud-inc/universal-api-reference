# Mendix: Get Project

Retrieves full project details from Mendix.

```
GET https://connect.mindcloud.co/v1/universal/mendix/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendix/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=d92064a5-b1fd-4be4-97db-53fc90201d1c" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "d92064a5-b1fd-4be4-97db-53fc90201d1c"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendix/latest/actions/get-project?${params}`, {
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
| `projectId` | string | yes | The unique identifier of a project. Example: `d92064a5-b1fd-4be4-97db-53fc90201d1c`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {
        "accountId": "string",
        "accountName": "Ava Chen"
      },
      "active": true,
      "categories": [
        {
          "categoryId": "string",
          "categoryName": "Ava Chen",
          "values": [
            {
              "code": "string",
              "value": "string"
            }
          ]
        }
      ],
      "cloudProvider": "string",
      "createdBy": {
        "fullName": "Ava Chen",
        "userId": "string"
      },
      "createdOn": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "logo": "string",
      "members": [
        {
          "avatarUrl": "https://example.com",
          "fullName": "Ava Chen",
          "isActive": true,
          "role": {
            "roleId": "string",
            "roleName": "Ava Chen"
          },
          "userId": "string"
        }
      ],
      "name": "Ava Chen",
      "projectId": "string",
      "storyBoardUrl": "https://example.com",
      "storyTool": "string",
      "targetCloud": "string",
      "technicalContact": {
        "fullName": "Ava Chen",
        "userId": "string"
      },
      "versionStudioPro": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account.accountId` | string | Unique identifier of the account. |
| `account.accountName` | string | Name of the account. |
| `active` | boolean | Indicates whether the project is active. |
| `categories[].categoryId` | string | Unique identifier of the project category. |
| `categories[].categoryName` | string | Name of the project category. |
| `categories[].values[].code` | string | Code of the assigned category value. |
| `categories[].values[].value` | string | Assigned category value. |
| `cloudProvider` | string | Cloud deployment provider. |
| `createdBy.fullName` | string | Full name of the user who created the project. |
| `createdBy.userId` | string | Unique identifier of the user who created the project. |
| `createdOn` | date | Date and time when the project was created. |
| `description` | string | Description of the project. |
| `logo` | string | URL of the project image or logo. |
| `members[].avatarUrl` | string | Avatar URL of a project member. |
| `members[].fullName` | string | Full name of a project member. |
| `members[].isActive` | boolean | Indicates whether the project member is active. |
| `members[].role.roleId` | string | Unique identifier of the member role. |
| `members[].role.roleName` | string | Name of the member role. |
| `members[].userId` | string | Unique identifier of a project member. |
| `name` | string | Name of the project. |
| `projectId` | string | Unique identifier for the project on the Mendix platform. |
| `storyBoardUrl` | string | URL of the project story board. |
| `storyTool` | string | Tool or service used to manage project workload. |
| `targetCloud` | string | URL of the cloud portal where the project is hosted. |
| `technicalContact.fullName` | string | Full name of the technical contact. |
| `technicalContact.userId` | string | Unique identifier of the technical contact. |
| `versionStudioPro` | string | Studio Pro version of the project's main branch. |

## Native endpoint

Through the native Mendix API, this operation is `GET /projects/:projectId` (base URL `https://projects-api.home.mendix.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

