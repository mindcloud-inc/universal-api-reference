# Infobip: Get Outbound SMS Delivery Reports



```
GET https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-outbound-sms-delivery-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-outbound-sms-delivery-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-outbound-sms-delivery-reports?${params}`, {
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
| `bulkId` | string | no | The ID that uniquely identifies the request. Bulk ID will be received only when you send a message to more than one destination address. |
| `messageId` | string | no | The ID that uniquely identifies the message sent. |
| `limit` | number | no | Maximum number of delivery reports to be returned. If not set, the latest 50 records are returned. Maximum limit value is 1000 and you can only access reports for the last 48h |
| `entityId` | string | no | Entity id used to send the message. For more details, see our [documentation](https://www.infobip.com/docs/cpaas-x/application-and-entity-management). |
| `applicationId` | string | no | Application id used to send the message. For more details, see our [documentation](https://www.infobip.com/docs/cpaas-x/application-and-entity-management). |
| `campaignReferenceId` | string | no | ID of a campaign that was sent in the message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": {
        "bulkId": "string",
        "callbackData": "string",
        "campaignReferenceId": "string",
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
        },
        "to": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> |  |
| `results.bulkId` | string |  |
| `results.callbackData` | string |  |
| `results.campaignReferenceId` | string |  |
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
| `results.to` | string |  |

## Native endpoint

Through the native Infobip API, this operation is `GET /sms/3/reports` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-outbound-sms-delivery-reports.md) for the provider-specific parameters and requirements.

