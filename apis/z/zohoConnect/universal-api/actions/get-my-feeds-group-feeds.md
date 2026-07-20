# Zoho Connect: Get My Feeds & Group Feeds

Retrieves your feeds and group feeds from Zoho Connect.

```
GET https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-my-feeds-group-feeds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-my-feeds-group-feeds?connectionId=$CONNECTION_ID&scopeId=string&lastViewedTime=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scopeId": "string",
  "lastViewedTime": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-my-feeds-group-feeds?${params}`, {
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
| `scopeId` | string | yes | ID of the network where the posts were made. |
| `partitionId` | string | no | Optional group ID to narrow the feed to a specific group wall. |
| `lastViewedTime` | number | yes | Fetch posts after this timestamp, in milliseconds. |
| `streamLimit` | number | no | Set a limit for the posts. |
| `fetchTime` | number | no | Fetch posts up to this timestamp, in milliseconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "getLatestStreams": {
        "count": "string",
        "streams": [
          {
            "allowFooter": "string",
            "canAddReminder": "string",
            "canAddRepetition": "string",
            "canAddTask": "string",
            "canDelete": "string",
            "canEdit": "string",
            "canFollow": "string",
            "canLock": "string",
            "canMarkAsReadLater": "string",
            "canMove": "string",
            "canShare": "string",
            "canShowPostAudit": "string",
            "canShowPostInsight": "string",
            "canTranslate": "string",
            "commentCount": "string",
            "comments": [
              {
                "canDelete": "string",
                "canEdit": "string",
                "canPinComment": "string",
                "canTranslate": "string",
                "commentType": "string",
                "content": "string",
                "formatedTime": "string",
                "id": "string",
                "isApproved": "string",
                "streamId": "string",
                "time": "string",
                "url": "https://example.com",
                "userDetails": {
                  "bgColor": "string",
                  "canFollow": "string",
                  "id": "string",
                  "imageUrl": "https://example.com",
                  "name": "Ava Chen",
                  "type": "string",
                  "zuid": "string"
                }
              }
            ],
            "content": "string",
            "dateComFormatStr": "string",
            "eEndDate": {
              "date": "string",
              "hour": "string",
              "minute": "string",
              "month": "string",
              "second": "string",
              "year": "string"
            },
            "endDate": "string",
            "endDay": "string",
            "endHour": "string",
            "endMin": "string",
            "endMonth": "string",
            "endTime": "string",
            "endYear": "string",
            "eStartDate": {
              "date": "string",
              "hour": "string",
              "minute": "string",
              "month": "string",
              "second": "string",
              "year": "string"
            },
            "event": {
              "attendeesCount": "string",
              "canAddReminderAll": "string",
              "canDelete": "string",
              "canEdit": "string",
              "desc": "string",
              "fieldPermission": {
                "canAddAssistant": "string",
                "canAddDesc": "string",
                "canAddEndTime": "string",
                "canAddInvitees": "string",
                "canAddLocation": "string",
                "canAddReminder": "string",
                "canAddRepetition": "string",
                "canAddRsvp": "string",
                "canAttachment": "string"
              },
              "isPrivateEvent": "string",
              "isRSVPAllowed": "string",
              "location": "string",
              "logoId": "string",
              "logoType": "string",
              "shortTitle": "string",
              "streamId": "string",
              "title": "string",
              "type": "string",
              "url": "https://example.com",
              "userDetails": {
                "canFollow": "string",
                "id": "string",
                "name": "Ava Chen",
                "zuid": "string"
              }
            },
            "eventEndTime": "string",
            "eventFullEndTime": "string",
            "eventFullStartTime": "string",
            "eventInvitedCount": "string",
            "eventInviteType": "string",
            "eventStartTime": "string",
            "formatedTime": "string",
            "formattedEndTime": "string",
            "formattedStartTime": "string",
            "fullformattedEndTime": "string",
            "fullformattedStartTime": "string",
            "googleCalendarUrl": "https://example.com",
            "id": "string",
            "isApproved": "string",
            "link": {
              "desc": "https://example.com",
              "linkurl": "https://example.com",
              "title": "https://example.com"
            },
            "module_name": "Ava Chen",
            "reason": {
              "msg": "string"
            },
            "startDate": "string",
            "startDay": "string",
            "startHour": "string",
            "startMin": "string",
            "startMonth": "string",
            "startTime": "string",
            "startYear": "string",
            "status": "string",
            "streamModifiedTime": "string",
            "time": "string",
            "title": "string",
            "type": "string",
            "uniqueViewCount": "string",
            "url": "https://example.com",
            "userDetails": {
              "canFollow": "string",
              "id": "string",
              "imageUrl": "https://example.com",
              "name": "Ava Chen",
              "type": "string",
              "zuid": "string"
            },
            "userIds": [
              {
                "id": "string",
                "imageUrl": "https://example.com",
                "name": "Ava Chen",
                "type": "string",
                "zuid": "string"
              }
            ],
            "viewCount": "string"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `getLatestStreams.count` | string |  |
| `getLatestStreams.streams[].allowFooter` | string |  |
| `getLatestStreams.streams[].canAddReminder` | string |  |
| `getLatestStreams.streams[].canAddRepetition` | string |  |
| `getLatestStreams.streams[].canAddTask` | string |  |
| `getLatestStreams.streams[].canDelete` | string |  |
| `getLatestStreams.streams[].canEdit` | string |  |
| `getLatestStreams.streams[].canFollow` | string |  |
| `getLatestStreams.streams[].canLock` | string |  |
| `getLatestStreams.streams[].canMarkAsReadLater` | string |  |
| `getLatestStreams.streams[].canMove` | string |  |
| `getLatestStreams.streams[].canShare` | string |  |
| `getLatestStreams.streams[].canShowPostAudit` | string |  |
| `getLatestStreams.streams[].canShowPostInsight` | string |  |
| `getLatestStreams.streams[].canTranslate` | string |  |
| `getLatestStreams.streams[].commentCount` | string |  |
| `getLatestStreams.streams[].comments[].canDelete` | string |  |
| `getLatestStreams.streams[].comments[].canEdit` | string |  |
| `getLatestStreams.streams[].comments[].canPinComment` | string |  |
| `getLatestStreams.streams[].comments[].canTranslate` | string |  |
| `getLatestStreams.streams[].comments[].commentType` | string |  |
| `getLatestStreams.streams[].comments[].content` | string |  |
| `getLatestStreams.streams[].comments[].formatedTime` | string |  |
| `getLatestStreams.streams[].comments[].id` | string |  |
| `getLatestStreams.streams[].comments[].isApproved` | string |  |
| `getLatestStreams.streams[].comments[].streamId` | string |  |
| `getLatestStreams.streams[].comments[].time` | string |  |
| `getLatestStreams.streams[].comments[].url` | string |  |
| `getLatestStreams.streams[].comments[].userDetails.bgColor` | string |  |
| `getLatestStreams.streams[].comments[].userDetails.canFollow` | string |  |
| `getLatestStreams.streams[].comments[].userDetails.id` | string |  |
| `getLatestStreams.streams[].comments[].userDetails.imageUrl` | string |  |
| `getLatestStreams.streams[].comments[].userDetails.name` | string |  |
| `getLatestStreams.streams[].comments[].userDetails.type` | string |  |
| `getLatestStreams.streams[].comments[].userDetails.zuid` | string |  |
| `getLatestStreams.streams[].content` | string |  |
| `getLatestStreams.streams[].dateComFormatStr` | string |  |
| `getLatestStreams.streams[].eEndDate.date` | string |  |
| `getLatestStreams.streams[].eEndDate.hour` | string |  |
| `getLatestStreams.streams[].eEndDate.minute` | string |  |
| `getLatestStreams.streams[].eEndDate.month` | string |  |
| `getLatestStreams.streams[].eEndDate.second` | string |  |
| `getLatestStreams.streams[].eEndDate.year` | string |  |
| `getLatestStreams.streams[].endDate` | string |  |
| `getLatestStreams.streams[].endDay` | string |  |
| `getLatestStreams.streams[].endHour` | string |  |
| `getLatestStreams.streams[].endMin` | string |  |
| `getLatestStreams.streams[].endMonth` | string |  |
| `getLatestStreams.streams[].endTime` | string |  |
| `getLatestStreams.streams[].endYear` | string |  |
| `getLatestStreams.streams[].eStartDate.date` | string |  |
| `getLatestStreams.streams[].eStartDate.hour` | string |  |
| `getLatestStreams.streams[].eStartDate.minute` | string |  |
| `getLatestStreams.streams[].eStartDate.month` | string |  |
| `getLatestStreams.streams[].eStartDate.second` | string |  |
| `getLatestStreams.streams[].eStartDate.year` | string |  |
| `getLatestStreams.streams[].event.attendeesCount` | string |  |
| `getLatestStreams.streams[].event.canAddReminderAll` | string |  |
| `getLatestStreams.streams[].event.canDelete` | string |  |
| `getLatestStreams.streams[].event.canEdit` | string |  |
| `getLatestStreams.streams[].event.desc` | string |  |
| `getLatestStreams.streams[].event.fieldPermission.canAddAssistant` | string |  |
| `getLatestStreams.streams[].event.fieldPermission.canAddDesc` | string |  |
| `getLatestStreams.streams[].event.fieldPermission.canAddEndTime` | string |  |
| `getLatestStreams.streams[].event.fieldPermission.canAddInvitees` | string |  |
| `getLatestStreams.streams[].event.fieldPermission.canAddLocation` | string |  |
| `getLatestStreams.streams[].event.fieldPermission.canAddReminder` | string |  |
| `getLatestStreams.streams[].event.fieldPermission.canAddRepetition` | string |  |
| `getLatestStreams.streams[].event.fieldPermission.canAddRsvp` | string |  |
| `getLatestStreams.streams[].event.fieldPermission.canAttachment` | string |  |
| `getLatestStreams.streams[].event.isPrivateEvent` | string |  |
| `getLatestStreams.streams[].event.isRSVPAllowed` | string |  |
| `getLatestStreams.streams[].event.location` | string |  |
| `getLatestStreams.streams[].event.logoId` | string |  |
| `getLatestStreams.streams[].event.logoType` | string |  |
| `getLatestStreams.streams[].event.shortTitle` | string |  |
| `getLatestStreams.streams[].event.streamId` | string |  |
| `getLatestStreams.streams[].event.title` | string |  |
| `getLatestStreams.streams[].event.type` | string |  |
| `getLatestStreams.streams[].event.url` | string |  |
| `getLatestStreams.streams[].event.userDetails.canFollow` | string |  |
| `getLatestStreams.streams[].event.userDetails.id` | string |  |
| `getLatestStreams.streams[].event.userDetails.name` | string |  |
| `getLatestStreams.streams[].event.userDetails.zuid` | string |  |
| `getLatestStreams.streams[].eventEndTime` | string |  |
| `getLatestStreams.streams[].eventFullEndTime` | string |  |
| `getLatestStreams.streams[].eventFullStartTime` | string |  |
| `getLatestStreams.streams[].eventInvitedCount` | string |  |
| `getLatestStreams.streams[].eventInviteType` | string |  |
| `getLatestStreams.streams[].eventStartTime` | string |  |
| `getLatestStreams.streams[].formatedTime` | string |  |
| `getLatestStreams.streams[].formattedEndTime` | string |  |
| `getLatestStreams.streams[].formattedStartTime` | string |  |
| `getLatestStreams.streams[].fullformattedEndTime` | string |  |
| `getLatestStreams.streams[].fullformattedStartTime` | string |  |
| `getLatestStreams.streams[].googleCalendarUrl` | string |  |
| `getLatestStreams.streams[].id` | string |  |
| `getLatestStreams.streams[].isApproved` | string |  |
| `getLatestStreams.streams[].link.desc` | string |  |
| `getLatestStreams.streams[].link.linkurl` | string |  |
| `getLatestStreams.streams[].link.title` | string |  |
| `getLatestStreams.streams[].module_name` | string |  |
| `getLatestStreams.streams[].reason.msg` | string |  |
| `getLatestStreams.streams[].startDate` | string |  |
| `getLatestStreams.streams[].startDay` | string |  |
| `getLatestStreams.streams[].startHour` | string |  |
| `getLatestStreams.streams[].startMin` | string |  |
| `getLatestStreams.streams[].startMonth` | string |  |
| `getLatestStreams.streams[].startTime` | string |  |
| `getLatestStreams.streams[].startYear` | string |  |
| `getLatestStreams.streams[].status` | string |  |
| `getLatestStreams.streams[].streamModifiedTime` | string |  |
| `getLatestStreams.streams[].time` | string |  |
| `getLatestStreams.streams[].title` | string |  |
| `getLatestStreams.streams[].type` | string |  |
| `getLatestStreams.streams[].uniqueViewCount` | string |  |
| `getLatestStreams.streams[].url` | string |  |
| `getLatestStreams.streams[].userDetails.canFollow` | string |  |
| `getLatestStreams.streams[].userDetails.id` | string |  |
| `getLatestStreams.streams[].userDetails.imageUrl` | string |  |
| `getLatestStreams.streams[].userDetails.name` | string |  |
| `getLatestStreams.streams[].userDetails.type` | string |  |
| `getLatestStreams.streams[].userDetails.zuid` | string |  |
| `getLatestStreams.streams[].userIds[].id` | string |  |
| `getLatestStreams.streams[].userIds[].imageUrl` | string |  |
| `getLatestStreams.streams[].userIds[].name` | string |  |
| `getLatestStreams.streams[].userIds[].type` | string |  |
| `getLatestStreams.streams[].userIds[].zuid` | string |  |
| `getLatestStreams.streams[].viewCount` | string |  |

## Native endpoint

Through the native Zoho Connect API, this operation is `GET /pulse/api/getLatestStreams` (base URL `https://connect.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-feeds-group-feeds.md) for the provider-specific parameters and requirements.

