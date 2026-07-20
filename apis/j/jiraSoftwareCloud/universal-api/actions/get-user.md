# Jira Software Cloud: Get User

Retrieves a user from Jira Software Cloud.

```
GET https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jira Software Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-user?connectionId=$CONNECTION_ID&accountId=string&cloudId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "cloudId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-user?${params}`, {
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
| `accountId` | string | yes | Atlassian account ID to fetch. |
| `cloudId` | string | yes | Jira cloud site ID returned by Accessible Resources. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "accountType": "string",
      "active": true,
      "avatarUrls": {
        "48x48": "https://example.com"
      },
      "displayName": "Ava Chen",
      "emailAddress": "ava@example.com",
      "locale": "string",
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `accountType` | string |  |
| `active` | boolean |  |
| `avatarUrls.48x48` | string |  |
| `displayName` | string |  |
| `emailAddress` | string |  |
| `locale` | string |  |
| `timeZone` | string |  |

## Native endpoint

Through the native Jira Software Cloud API, this operation is `GET /ex/jira/:cloudId/rest/api/3/user` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

