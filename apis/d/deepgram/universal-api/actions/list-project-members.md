# Deepgram: List Project Members

Retrieves project members from Deepgram.

```
GET https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/list-project-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepgram `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/list-project-members?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/list-project-members?${params}`, {
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
      "firstName": "Ava",
      "lastName": "Chen",
      "memberId": "string",
      "scopes": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Member email address. |
| `firstName` | string | Member first name. |
| `lastName` | string | Member last name. |
| `memberId` | string | Deepgram member identifier. |
| `scopes` | array<string> | Scopes granted to the project member. |

## Native endpoint

Through the native Deepgram API, this operation is `GET /v1/projects/:project_id/members` (base URL `https://api.deepgram.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-members.md) for the provider-specific parameters and requirements.

