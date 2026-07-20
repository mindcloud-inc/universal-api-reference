# Audienceful: Delete Person

Deletes an existing person from Audienceful.

```
DELETE https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/delete-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Audienceful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/delete-person?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/delete-person?${params}`, {
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
| `email` | string | yes | The email of the person you wish to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "extraData": {},
      "lastActivity": "2026-05-07T12:00:00.000Z",
      "notes": "string",
      "status": "string",
      "tags": [
        {}
      ],
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the person record was created. |
| `email` | string | Email address for the person. |
| `extraData` | object | Provider-specific supplemental person attributes. |
| `lastActivity` | date | Last tracked activity time for the person. |
| `notes` | string | Notes associated with the person. |
| `status` | string | Current Audienceful person status. |
| `tags` | array<object> | Tags assigned to the person. |
| `uid` | string | Audienceful person UID. |

## Native endpoint

Through the native Audienceful API, this operation is `DELETE /people/` (base URL `https://app.audienceful.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-person.md) for the provider-specific parameters and requirements.

