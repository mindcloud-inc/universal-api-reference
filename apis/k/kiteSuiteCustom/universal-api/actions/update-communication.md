# Kite Suite: Update communication



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-communication
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-communication" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-communication', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Update field ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "accountID": "string",
      "action": "string",
      "attachments": [
        "string"
      ],
      "bcc": [
        "string"
      ],
      "body": "string",
      "campaignID": "string",
      "cc": [
        "string"
      ],
      "communicationID": "string",
      "createdAt": "string",
      "createdBy": "string",
      "insertUnsubscribeLink": true,
      "isAutoReply": true,
      "isMainThread": true,
      "isTextOnly": true,
      "isTrashed": true,
      "itemID": "string",
      "lastUpdated": "string",
      "leadID": "string",
      "linkTrack": [
        "https://example.com"
      ],
      "linkTracking": true,
      "openTracking": true,
      "receivers": [
        "string"
      ],
      "responseData": {},
      "sender": "string",
      "sentAt": "string",
      "status": "string",
      "subject": "string",
      "tracking": [
        "string"
      ],
      "type": "string",
      "updatedAt": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | Unique identifier for the communication |
| `accountID` | string | Reference to email account |
| `action` | string | Action associated with communication |
| `attachments` | array |  |
| `bcc` | array<string> | Email addresses in bcc |
| `body` | string | Email body content |
| `campaignID` | string | Reference to campaign |
| `cc` | array<string> | Email addresses in cc |
| `communicationID` | string | Reference to parent communication |
| `createdAt` | string |  |
| `createdBy` | string | Reference to user who created the communication |
| `insertUnsubscribeLink` | boolean |  |
| `isAutoReply` | boolean |  |
| `isMainThread` | boolean |  |
| `isTextOnly` | boolean |  |
| `isTrashed` | boolean | Whether the communication is trashed |
| `itemID` | string | Reference to task |
| `lastUpdated` | string |  |
| `leadID` | string | Reference to campaign lead |
| `linkTrack` | array |  |
| `linkTracking` | boolean |  |
| `openTracking` | boolean |  |
| `receivers` | array<string> | Email addresses of receivers |
| `responseData` | object | Response data object |
| `sender` | string | Email address of sender |
| `sentAt` | string |  |
| `status` | string | Status of the communication |
| `subject` | string | Email subject |
| `tracking` | array |  |
| `type` | string | Type of communication |
| `updatedAt` | string |  |
| `workspace` | string | Reference to workspace |

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/communication/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-communication.md) for the provider-specific parameters and requirements.

