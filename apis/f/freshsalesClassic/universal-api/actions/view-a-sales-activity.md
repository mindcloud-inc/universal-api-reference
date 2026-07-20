# Freshsales Classic: View a Sales Activity

Retrieves a sales activity from Freshsales Classic.

```
GET https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/view-a-sales-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshsales Classic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/view-a-sales-activity?connectionId=$CONNECTION_ID&salesActivityId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "salesActivityId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/view-a-sales-activity?${params}`, {
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
| `salesActivityId` | number | yes | The sales activity ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalUserCount": 1,
      "checkedinAt": "string",
      "checkedinDuration": 1,
      "checkedoutAt": "string",
      "checkedoutLatitude": "string",
      "checkedoutLocation": "string",
      "checkedoutLongitude": "string",
      "completedDate": "string",
      "conversationId": 1,
      "conversationTime": "string",
      "createdAt": "string",
      "createrId": 1,
      "customField": {},
      "endDate": "string",
      "hasMultipleEmails": true,
      "id": 1,
      "importId": "string",
      "latitude": "string",
      "location": "string",
      "longitude": "string",
      "noteId": 1,
      "notes": "string",
      "ownerId": 1,
      "remoteId": "string",
      "salesActivityOutcomeId": 1,
      "salesActivityTypeId": 1,
      "startDate": "string",
      "status": true,
      "targetableId": 1,
      "targetables": [
        {}
      ],
      "targetablesWithEmail": [
        {}
      ],
      "targetableType": "string",
      "title": "string",
      "updatedAt": "string",
      "updaterId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalUserCount` | number | Count of additional associated users when present. |
| `checkedinAt` | string | Timestamp of the check-in when present. |
| `checkedinDuration` | number | Duration spent checked in, in seconds, when present. |
| `checkedoutAt` | string | Checkout timestamp when present. |
| `checkedoutLatitude` | string | Latitude captured at checkout when present. |
| `checkedoutLocation` | string | Location captured at checkout when present. |
| `checkedoutLongitude` | string | Longitude captured at checkout when present. |
| `completedDate` | string | Completion timestamp when present. |
| `conversationId` | number | Conversation ID linked to the sales activity when present. |
| `conversationTime` | string | Conversation timestamp associated with the activity when present. |
| `createdAt` | string | Sales activity creation timestamp. |
| `createrId` | number | ID of the user who created the sales activity. |
| `customField` | object | Custom field payload for the sales activity when present. |
| `endDate` | string | End timestamp of the sales activity. |
| `hasMultipleEmails` | boolean | Whether multiple target emails are associated. |
| `id` | number | Unique ID of the sales activity. |
| `importId` | string | Import identifier when present. |
| `latitude` | string | Latitude captured for the activity location when present. |
| `location` | string | Location associated with the sales activity when present. |
| `longitude` | string | Longitude captured for the activity location when present. |
| `noteId` | number | Note ID associated with the sales activity when present. |
| `notes` | string | Description or notes for the sales activity. |
| `ownerId` | number | ID of the user who owns the sales activity. |
| `remoteId` | string | Remote identifier when present. |
| `salesActivityOutcomeId` | number | ID of the selected sales activity outcome when present. |
| `salesActivityTypeId` | number | ID of the sales activity type. |
| `startDate` | string | Start timestamp of the sales activity. |
| `status` | boolean | Whether the sales activity is marked completed. |
| `targetableId` | number | ID of the related contact, account, or deal. |
| `targetables` | array<object> | Related target entities for the sales activity. |
| `targetablesWithEmail` | array<object> | Related target entities with display names. |
| `targetableType` | string | Entity type related to the sales activity. |
| `title` | string | Title of the sales activity. |
| `updatedAt` | string | Sales activity update timestamp. |
| `updaterId` | number | ID of the user who last updated the sales activity when present. |

## Native endpoint

Through the native Freshsales Classic API, this operation is `GET /sales_activities/:salesActivityId` (base URL `https://{{credentials.bundleAlias}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-a-sales-activity.md) for the provider-specific parameters and requirements.

