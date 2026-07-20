# Infobip: Get Outbound SMS Message Logs



```
GET https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-outbound-sms-message-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-outbound-sms-message-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-outbound-sms-message-logs?${params}`, {
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
| `mcc` | string | no | Mobile Country Code. |
| `mnc` | string | no | Mobile Network Code. Mobile Country Code is required if this property is used. |
| `sender` | string | no | The sender ID which can be alphanumeric or numeric. |
| `destination` | string | no | Message destination address. |
| `bulkId` | list<string> | no | Unique ID assigned to the request if messaging multiple recipients or sending multiple messages via a single API request. May contain multiple comma-separated values. Maximum length 2048 characters. |
| `messageId` | list<string> | no | Unique message ID for which a log is requested. May contain multiple comma-separated values. Maximum length 2048 characters. |
| `generalStatus` | string | no |  |
| `sentSince` | date | no | The logs will only include messages sent after this date. Use it alongside sentUntil to specify a time range for the logs, but only up to the maximum limit of 1000 logs per call. Has the following format: yyyy-MM-dd'T'HH:mm:ss.SSSZ. |
| `sentUntil` | date | no | The logs will only include messages sent before this date. Use it alongside sentSince to specify a time range for the logs, but only up to the maximum limit of 1000 logs per call. Has the following format: yyyy-MM-dd'T'HH:mm:ss.SSSZ. |
| `limit` | number | no | Maximum number of messages to include in logs. If not set, the latest 50 records are returned. Maximum limit value is 1000 and you can only access logs for the last 48h. |
| `entityId` | string | no | Entity id used to send the message. For more details, see our [documentation](https://www.infobip.com/docs/cpaas-x/application-and-entity-management). |
| `applicationId` | string | no | Application id used to send the message. For more details, see our [documentation](https://www.infobip.com/docs/cpaas-x/application-and-entity-management). |
| `campaignReferenceId` | list<string> | no | ID of a campaign that was sent in the message. May contain multiple comma-separated values. |
| `useCursor` | boolean | no | Flag used to enable cursor-based pagination. When set to true, the system will use the cursor to fetch the next set of logs. |
| `cursor` | string | no | Value which represents the current position in the data set. For the first request, this field shouldn't be defined. In subsequent requests, use the `nextCursor` value returned from the previous response to continue fetching data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": {
        "limit": 1,
        "nextCursor": "string"
      },
      "results": {
        "bulkId": "string",
        "campaignReferenceId": "string",
        "content": {},
        "destination": "string",
        "doneAt": "2026-05-07T12:00:00.000Z",
        "error": {
          "description": "string",
          "groupId": 1,
          "groupName": "Ava Chen",
          "id": 1,
          "name": "Ava Chen",
          "permanent": true
        },
        "mccMnc": "string",
        "messageCount": 1,
        "messageId": "string",
        "platform": {
          "applicationId": "string",
          "entityId": "string"
        },
        "price": {
          "currency": "string",
          "pricePerMessage": 1
        },
        "sender": "string",
        "sentAt": "2026-05-07T12:00:00.000Z",
        "status": {
          "action": "string",
          "description": "string",
          "groupId": 1,
          "groupName": "Ava Chen",
          "id": 1,
          "name": "Ava Chen"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cursor` | object |  |
| `cursor.limit` | number |  |
| `cursor.nextCursor` | string |  |
| `results` | array<object> |  |
| `results.bulkId` | string |  |
| `results.campaignReferenceId` | string |  |
| `results.content` | object |  |
| `results.destination` | string |  |
| `results.doneAt` | date |  |
| `results.error` | object |  |
| `results.error.description` | string |  |
| `results.error.groupId` | number |  |
| `results.error.groupName` | string |  |
| `results.error.id` | number |  |
| `results.error.name` | string |  |
| `results.error.permanent` | boolean |  |
| `results.mccMnc` | string |  |
| `results.messageCount` | number |  |
| `results.messageId` | string |  |
| `results.platform` | object |  |
| `results.platform.applicationId` | string |  |
| `results.platform.entityId` | string |  |
| `results.price` | object |  |
| `results.price.currency` | string |  |
| `results.price.pricePerMessage` | number |  |
| `results.sender` | string |  |
| `results.sentAt` | date |  |
| `results.status` | object |  |
| `results.status.action` | string |  |
| `results.status.description` | string |  |
| `results.status.groupId` | number |  |
| `results.status.groupName` | string |  |
| `results.status.id` | number |  |
| `results.status.name` | string |  |

## Native endpoint

Through the native Infobip API, this operation is `GET /sms/3/logs` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-outbound-sms-message-logs.md) for the provider-specific parameters and requirements.

