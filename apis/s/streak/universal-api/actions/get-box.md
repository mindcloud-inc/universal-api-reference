# Streak: Get Box

Retrieves a box from Streak.

```
GET https://connect.mindcloud.co/v1/universal/streak/latest/actions/get-box
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streak/latest/actions/get-box?connectionId=$CONNECTION_ID&boxKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "boxKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streak/latest/actions/get-box?${params}`, {
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
| `boxKey` | string | yes | The key of the box to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedToSharingEntries": [
        {}
      ],
      "boxKey": "string",
      "callLogCount": 1,
      "commentCount": 1,
      "creationSourceType": "string",
      "creationTimestamp": "2026-05-07T12:00:00.000Z",
      "creatorKey": "string",
      "creatorSharingEntry": {},
      "emailAddresses": [
        "ava@example.com"
      ],
      "emailAddressesAutoExtracted": [
        "ava@example.com"
      ],
      "emailAddressesBlacklist": [
        "ava@example.com"
      ],
      "fields": {},
      "fieldsAutofillStatus": {},
      "fileCount": 1,
      "followerCount": 1,
      "followerKeys": [
        "string"
      ],
      "followerSharingEntries": [
        {}
      ],
      "freshness": 1,
      "gmailThreadCount": 1,
      "incompleteTaskAssigneeKeySet": [
        "string"
      ],
      "incompleteTaskAssigneeSharingEntrySet": [
        {}
      ],
      "key": "string",
      "lastSavedTimestamp": "2026-05-07T12:00:00.000Z",
      "lastStageChangeTimestamp": "2026-05-07T12:00:00.000Z",
      "lastUpdatedTimestamp": "2026-05-07T12:00:00.000Z",
      "linkedBoxKeys": [
        "https://example.com"
      ],
      "meetingNotesCount": 1,
      "name": "Ava Chen",
      "notes": "string",
      "overdueTaskAssigneeKeySet": [
        "string"
      ],
      "overdueTaskAssigneeSharingEntrySet": [
        {}
      ],
      "pipelineKey": "string",
      "stageHistoryEntries": [
        {}
      ],
      "stageKey": "string",
      "taskAssigneeKeySet": [
        "string"
      ],
      "taskAssigneeSharingEntrySet": [
        {}
      ],
      "taskCompleteCount": 1,
      "taskIncompleteCount": 1,
      "taskOverdueCount": 1,
      "taskPercentageComplete": 1,
      "taskTotal": 1,
      "totalCallLogDuration": 1,
      "totalMeetingNotesDuration": 1,
      "totalNumberOfEmails": 1,
      "totalNumberOfLastSentEmailLinksClicks": 1,
      "totalNumberOfLastSentEmailViews": 1,
      "totalNumberOfReceivedEmails": 1,
      "totalNumberOfSentEmails": 1,
      "totalNumberOfSentEmailsViews": 1,
      "violations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedToSharingEntries` | array<object> | The users assigned to the box. |
| `boxKey` | string | The box identifier. |
| `callLogCount` | number | The number of call logs on the box. |
| `commentCount` | number | The number of comments on the box. |
| `creationSourceType` | string | How the box was created. |
| `creationTimestamp` | date | When the box was created. |
| `creatorKey` | string | The user who created the box. |
| `creatorSharingEntry` | object | The creator sharing entry. |
| `emailAddresses` | array<string> | Email addresses associated with the box. |
| `emailAddressesAutoExtracted` | array<string> | Email addresses auto-extracted for the box. |
| `emailAddressesBlacklist` | array<string> | Blacklisted email addresses for the box. |
| `fields` | object | The box field values keyed by field ID. |
| `fieldsAutofillStatus` | object | Autofill status keyed by field ID. |
| `fileCount` | number | The number of files linked to the box. |
| `followerCount` | number | The number of followers on the box. |
| `followerKeys` | array<string> | The follower user keys. |
| `followerSharingEntries` | array<object> | The users following the box. |
| `freshness` | number | The freshness score for the box. |
| `gmailThreadCount` | number | The number of Gmail threads linked to the box. |
| `incompleteTaskAssigneeKeySet` | array<string> | The user keys assigned to incomplete tasks. |
| `incompleteTaskAssigneeSharingEntrySet` | array<object> | The sharing entries for incomplete task assignees. |
| `key` | string | The box key alias. |
| `lastSavedTimestamp` | date | When the box was last saved. |
| `lastStageChangeTimestamp` | date | When the box last changed stages. |
| `lastUpdatedTimestamp` | date | When the box was last updated. |
| `linkedBoxKeys` | array<string> | The linked box keys. |
| `meetingNotesCount` | number | The number of meeting notes on the box. |
| `name` | string | The box name. |
| `notes` | string | The notes of the box. |
| `overdueTaskAssigneeKeySet` | array<string> | The user keys assigned to overdue tasks. |
| `overdueTaskAssigneeSharingEntrySet` | array<object> | The sharing entries for overdue task assignees. |
| `pipelineKey` | string | The pipeline the box belongs to. |
| `stageHistoryEntries` | array<object> | The box stage history entries. |
| `stageKey` | string | The current stage key. |
| `taskAssigneeKeySet` | array<string> | The user keys assigned to tasks. |
| `taskAssigneeSharingEntrySet` | array<object> | The sharing entries for task assignees. |
| `taskCompleteCount` | number | The number of completed tasks. |
| `taskIncompleteCount` | number | The number of incomplete tasks. |
| `taskOverdueCount` | number | The number of overdue tasks. |
| `taskPercentageComplete` | number | The percentage of tasks completed. |
| `taskTotal` | number | The total number of tasks. |
| `totalCallLogDuration` | number | The total duration of call logs. |
| `totalMeetingNotesDuration` | number | The total duration of meeting notes. |
| `totalNumberOfEmails` | number | The total number of emails on the box. |
| `totalNumberOfLastSentEmailLinksClicks` | number | The total number of link clicks on the last sent email. |
| `totalNumberOfLastSentEmailViews` | number | The total number of views on the last sent email. |
| `totalNumberOfReceivedEmails` | number | The total number of received emails on the box. |
| `totalNumberOfSentEmails` | number | The total number of sent emails on the box. |
| `totalNumberOfSentEmailsViews` | number | The total number of views across sent emails. |
| `violations` | array<object> | Any recorded box violations. |

## Native endpoint

Through the native Streak API, this operation is `GET /api/v1/boxes/:boxKey` (base URL `https://api.streak.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-box.md) for the provider-specific parameters and requirements.

