# CRUSH: Get Note



```
GET https://connect.mindcloud.co/v1/universal/cRUSH/latest/actions/get-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CRUSH `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cRUSH/latest/actions/get-note?connectionId=$CONNECTION_ID&noteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "noteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cRUSH/latest/actions/get-note?${params}`, {
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
| `noteId` | string | yes | The CRUSH note ID to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "folderId": "string",
      "insightId": "string",
      "mediaIsAttached": true,
      "mediaIsUnread": true,
      "noteAudioStatus": "string",
      "noteCheckboxState": "string",
      "noteCreatedById": "string",
      "noteCreatedOn": "2026-05-07T12:00:00.000Z",
      "noteId": "string",
      "noteIsArchived": true,
      "noteIsDeleted": true,
      "noteIsKeepAudio": true,
      "noteIsShared": true,
      "noteIsUnread": true,
      "noteLastEdited": "2026-05-07T12:00:00.000Z",
      "noteMemberIds": [
        "string"
      ],
      "noteRuleStatus": "string",
      "noteTranscript": "string",
      "noteTranscriptDraft": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userChatId": "string",
      "userChatIsUnread": true,
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the note flag row was created. |
| `folderId` | string | Folder ID the note belongs to, when present. |
| `insightId` | string | Linked insight ID, when present. |
| `mediaIsAttached` | boolean | Whether the note has media attachments. |
| `mediaIsUnread` | boolean | Whether attached media is unread. |
| `noteAudioStatus` | string | Audio processing status for the note. |
| `noteCheckboxState` | string | Checklist state for the note. |
| `noteCreatedById` | string | User ID that created the note. |
| `noteCreatedOn` | date | When the note was originally created. |
| `noteId` | string | Unique note identifier. |
| `noteIsArchived` | boolean | Whether the note is archived. |
| `noteIsDeleted` | boolean | Whether the note is deleted. |
| `noteIsKeepAudio` | boolean | Whether original audio is preserved for the note. |
| `noteIsShared` | boolean | Whether the note is shared. |
| `noteIsUnread` | boolean | Whether the note is unread. |
| `noteLastEdited` | date | When the note content was last edited. |
| `noteMemberIds` | array<string> | Member IDs associated with the note. |
| `noteRuleStatus` | string | Rule-processing status for the note. |
| `noteTranscript` | string | Transcript text for the note. |
| `noteTranscriptDraft` | string | Draft transcript content, when present. |
| `updatedAt` | date | When the note flag row was last updated. |
| `userChatId` | string | Associated chat ID, when present. |
| `userChatIsUnread` | boolean | Whether the associated chat is unread. |
| `userId` | string | User ID for the returned note-flag row. |

## Native endpoint

Through the native CRUSH API, this operation is `GET /aws/noteflags` (base URL `https://app.crushthememory.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-note.md) for the provider-specific parameters and requirements.

