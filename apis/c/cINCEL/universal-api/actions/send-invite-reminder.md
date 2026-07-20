# CINCEL: Send Invite Reminder



```
GET https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/send-invite-reminder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CINCEL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/send-invite-reminder?connectionId=$CONNECTION_ID&team=string&folder=string&document=string&invite=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "team": "string",
  "folder": "string",
  "document": "string",
  "invite": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/send-invite-reminder?${params}`, {
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
| `team` | string | yes | Team UUID from the path. |
| `folder` | string | yes | Folder UUID from the path. |
| `document` | string | yes | Document UUID from the path. |
| `invite` | string | yes | Invite UUID from the path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Reminder delivery message returned by the provider. |
| `statusCode` | number | HTTP-style status code returned by the provider. |

## Native endpoint

Through the native CINCEL API, this operation is `GET /teams/:team/folders/:folder/documents/:document/invites/:invite/notification` (base URL `https://api.cincel.digital/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-invite-reminder.md) for the provider-specific parameters and requirements.

