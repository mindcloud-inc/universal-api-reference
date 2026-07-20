# Streak Universal API Examples

These examples use the MindCloud API key and Streak connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Streak.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streak/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streak/latest/actions/get-current-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "canceledTrial": true,
      "creationTimestamp": 1,
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "firstExtension": "string",
      "firstOauthTimestamp": 1,
      "googleAnalyticsClientId": "string",
      "googleProfileFirstName": "Ava",
      "googleProfileFullName": "Ava Chen",
      "googleProfileGender": "string",
      "googleProfileId": "string",
      "googleProfileLastName": "Chen",
      "googleProfileLink": "https://example.com",
      "googleProfileLocale": "string",
      "googleProfilePhotoUrl": "https://example.com",
      "hasCancellationDiscount": true,
      "intercomHmac": "string",
      "isOauthComplete": true,
      "key": "string",
      "lastProPlusTrialStart": 1,
      "lastSavedTimestamp": 1,
      "lastSeenTimestamp": 1,
      "lastTrialLength": 1,
      "lastTrialStart": 1,
      "lastUpdatedTimestamp": 1,
      "onTrialWithoutCreditCard": true,
      "orgKey": "string",
      "timezoneId": "string",
      "tourId": "string",
      "usedPlatforms": [
        {}
      ],
      "userKey": "string",
      "userSettingsKey": "string",
      "userSource": "string",
      "wantsTaskDigestEmail": true
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/streak/latest/actions/get-current-user).

## Create Box

Creates a new box in Streak.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/streak/latest/actions/create-box" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pipelineKey": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/streak/latest/actions/create-box', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pipelineKey": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

Example response:

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

See the full [Create Box action reference](actions/create-box.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/streak/latest/actions/create-box).
