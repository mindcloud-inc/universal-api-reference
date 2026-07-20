# Streak: List Box Threads

Retrieves threads for a box in Streak.

```
GET https://connect.mindcloud.co/v1/universal/streak/latest/actions/list-box-threads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streak/latest/actions/list-box-threads?connectionId=$CONNECTION_ID&boxKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "boxKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streak/latest/actions/list-box-threads?${params}`, {
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
| `boxKey` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "boxKey": "string",
      "creationTimestamp": "2026-05-07T12:00:00.000Z",
      "creatorKey": "string",
      "emailAddresses": [
        "ava@example.com"
      ],
      "fileKeys": [
        "string"
      ],
      "files": [
        {}
      ],
      "gmailThreadKey": "string",
      "key": "string",
      "lastUpdatedTimestamp": "2026-05-07T12:00:00.000Z",
      "names": [
        "Ava Chen"
      ],
      "pipelineKey": "string",
      "threadGmailId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `boxKey` | string | The box that owns the thread. |
| `creationTimestamp` | date | When the thread was created. |
| `creatorKey` | string | The user who created the thread. |
| `emailAddresses` | array<string> | Participant email addresses on the thread. |
| `fileKeys` | array<string> | File keys linked to the thread. |
| `files` | array<object> | Files linked to the thread. |
| `gmailThreadKey` | string | The Streak Gmail thread key. |
| `key` | string | The thread key. |
| `lastUpdatedTimestamp` | date | When the thread was last updated. |
| `names` | array<string> | Participant names on the thread. |
| `pipelineKey` | string | The pipeline that owns the thread. |
| `threadGmailId` | string | The Gmail thread identifier. |

## Native endpoint

Through the native Streak API, this operation is `GET /api/v1/boxes/:boxKey/threads` (base URL `https://api.streak.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-box-threads.md) for the provider-specific parameters and requirements.

