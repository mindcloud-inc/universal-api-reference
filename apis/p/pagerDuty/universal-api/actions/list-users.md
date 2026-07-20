# PagerDuty: List Users



```
GET https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PagerDuty `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/list-users?${params}`, {
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
| `query` | string | no | Filter users by a free-text search query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarUrl": "https://example.com",
      "billed": true,
      "color": "string",
      "contactMethods": [
        {
          "htmlUrl": "https://example.com",
          "id": "string",
          "self": "string",
          "summary": "string",
          "type": "string"
        }
      ],
      "coordinatedIncidents": [
        "string"
      ],
      "createdViaSso": true,
      "description": "string",
      "email": "ava@example.com",
      "htmlUrl": "https://example.com",
      "id": "string",
      "invitationSent": true,
      "jobTitle": "string",
      "locale": "string",
      "name": "Ava Chen",
      "notificationRules": [
        {
          "htmlUrl": "https://example.com",
          "id": "string",
          "self": "string",
          "summary": "string",
          "type": "string"
        }
      ],
      "role": "string",
      "self": "string",
      "summary": "string",
      "teams": [
        "string"
      ],
      "timeZone": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string | The user's avatar image URL. |
| `billed` | boolean | Whether the user is a billed user. |
| `color` | string | The PagerDuty color assigned to the user. |
| `contactMethods` | array<object> | The user's contact methods. |
| `contactMethods[].htmlUrl` | string | The PagerDuty web URL for the contact method. |
| `contactMethods[].id` | string | The contact method ID. |
| `contactMethods[].self` | string | The API URL for the contact method. |
| `contactMethods[].summary` | string | PagerDuty's short summary for the contact method. |
| `contactMethods[].type` | string | The contact method type. |
| `coordinatedIncidents` | array | Incidents coordinated by the user. |
| `createdViaSso` | boolean | Whether the user was created via SSO. |
| `description` | string | The user's profile description. |
| `email` | string | The user's email address. |
| `htmlUrl` | string | The PagerDuty web URL for the user. |
| `id` | string | The PagerDuty user ID. |
| `invitationSent` | boolean | Whether an invitation has been sent to the user. |
| `jobTitle` | string | The user's job title. |
| `locale` | string | The user's locale. |
| `name` | string | The user's display name. |
| `notificationRules` | array<object> | The user's notification rules. |
| `notificationRules[].htmlUrl` | string | The PagerDuty web URL for the notification rule. |
| `notificationRules[].id` | string | The notification rule ID. |
| `notificationRules[].self` | string | The API URL for the notification rule. |
| `notificationRules[].summary` | string | PagerDuty's short summary for the notification rule. |
| `notificationRules[].type` | string | The notification rule type. |
| `role` | string | The user's PagerDuty role. |
| `self` | string | The API URL for the user. |
| `summary` | string | PagerDuty's short summary for the user. |
| `teams` | array | The teams the user belongs to. |
| `timeZone` | string | The user's configured time zone. |
| `type` | string | The PagerDuty object type. |

## Native endpoint

Through the native PagerDuty API, this operation is `GET /users` (base URL `https://api.pagerduty.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

