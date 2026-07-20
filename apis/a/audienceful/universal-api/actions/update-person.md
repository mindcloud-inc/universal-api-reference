# Audienceful: Update Person

Updates an existing person in Audienceful.

```
PUT https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/update-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Audienceful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/update-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/update-person', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The person's email. |
| `tags[]` | array<string> | no | Comma-separated tags. Missing tags are created. |
| `notes` | string | no | Notes associated with this person. |
| `extraData` | object | no | Custom field payload for this person. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bounced": true,
      "clickRate": 1,
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "doubleOptIn": "string",
      "email": "ava@example.com",
      "extraData": {},
      "id": 1,
      "lastActivity": "2026-05-07T12:00:00.000Z",
      "openRate": 1,
      "source": "string",
      "status": "string",
      "tags": [
        "string"
      ],
      "uid": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounced` | boolean | Whether the email address has bounced. |
| `clickRate` | number | Aggregate click rate for the person. |
| `country` | string | Country value stored on the person record. |
| `createdAt` | date | When the person record was created. |
| `doubleOptIn` | string | Double opt-in state for the person. |
| `email` | string | Email address for the person. |
| `extraData` | object | Provider-specific supplemental person attributes. |
| `id` | number | Audienceful person ID. |
| `lastActivity` | date | Last tracked activity time for the person. |
| `openRate` | number | Aggregate open rate for the person. |
| `source` | string | Audienceful acquisition source for the person. |
| `status` | string | Current Audienceful person status. |
| `tags` | array<string> | Tags assigned to the person. |
| `uid` | string | Audienceful person UID. |
| `updatedAt` | date | When the person record was last updated. |

## Native endpoint

Through the native Audienceful API, this operation is `PATCH /people/` (base URL `https://app.audienceful.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-person.md) for the provider-specific parameters and requirements.

