# Deepgram: List Project Invites

Retrieves project invites from Deepgram.

```
GET https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/list-project-invites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepgram `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/list-project-invites?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/list-project-invites?${params}`, {
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
| `projectId` | string | yes | The Deepgram project identifier to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "scope": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Invitee email address. |
| `scope` | string | Scope requested by the invite. |

## Native endpoint

Through the native Deepgram API, this operation is `GET /v1/projects/:project_id/invites` (base URL `https://api.deepgram.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-invites.md) for the provider-specific parameters and requirements.

