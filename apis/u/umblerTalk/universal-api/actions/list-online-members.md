# Umbler Talk: List Online Members

Retrieves online members from Umbler Talk.

```
GET https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/list-online-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbler Talk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/list-online-members?connectionId=$CONNECTION_ID&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/list-online-members?${params}`, {
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
| `organizationId` | string | yes | The organization ID. Use Get Current Member to find available organizations. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_t": "string",
      "active": true,
      "billable": true,
      "displayName": "Ava Chen",
      "emailAddress": "ava@example.com",
      "id": "string",
      "lastBotTransferenceUTC": "2026-05-07T12:00:00.000Z",
      "permissions": [
        "string"
      ],
      "profilePictureUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_t` | string |  |
| `active` | boolean |  |
| `billable` | boolean |  |
| `displayName` | string |  |
| `emailAddress` | string |  |
| `id` | string |  |
| `lastBotTransferenceUTC` | date |  |
| `permissions` | array<string> |  |
| `profilePictureUrl` | string |  |

## Native endpoint

Through the native Umbler Talk API, this operation is `GET /v1/members/online/` (base URL `https://app-utalk.umbler.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-online-members.md) for the provider-specific parameters and requirements.

