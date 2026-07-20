# Infobip: Send SMS Message



```
POST https://connect.mindcloud.co/v1/universal/infobip/latest/actions/send-sms-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/send-sms-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messages": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infobip/latest/actions/send-sms-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messages": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messages` | list<object> | yes | An array of message objects of a single message or multiple messages sent under one bulk ID. |
| `messages.sender` | string | no | The sender ID. It can be alphanumeric or numeric (e.g., `CompanyName`). Make sure you don't exceed [character limit](https://www.infobip.com/docs/sms/get-started#sender-names). |
| `messages.destinations` | list<object> | no | An array of destination objects for where messages are being sent. A valid destination is required. |
| `messages.content` | object | no | Message content. |
| `messages.options` | object | no | Message options. |
| `messages.options.platform` | object | no | Platform options. For more details, see [documentation](https://www.infobip.com/docs/cpaas-x/application-and-entity-management). |
| `messages.options.validityPeriod` | object | no | Message validity period. Once expired, the message won't be sent. Validity period longer than 48h is not supported. If exceeded, it will be automatically set to 48h. |
| `messages.options.deliveryTimeWindow` | object | no | Sets specific message delivery window outside of which messages won't be delivered. Often, used when there are restrictions on when messages can be sent. The exact time of the day to start sending messages can be defined using the `from` property. The exact time of the day to end sending messages can be defined using the `to` property. Properties `from` and `to` should be both provided with the minimum 1 hour difference or omitted. |
| `messages.options.campaignReferenceId` | string | no | ID that allows you to track, analyze, and show an aggregated overview and the performance of individual campaigns per sending channel. |
| `messages.options.regional` | object | no | Region-specific parameters, often imposed by local laws. Use this, if country or region that you are sending an SMS to requires additional information. |
| `messages.options.flash` | boolean | no | Allows for sending a [flash SMS](https://www.infobip.com/docs/sms/message-types#flash-sms) to automatically appear on recipient devices without interaction. Set to `true` to enable flash SMS, or leave the default value, `false` to send a standard SMS. |
| `messages.webhooks` | object | no | Provides options for configuring message webhooks. |
| `messages.webhooks.delivery` | object | no | Provides options for configuring the delivery report behavior. |
| `messages.webhooks.contentType` | string | no | Preferred delivery report content type, `application/json` or `application/xml`. |
| `messages.webhooks.callbackData` | string | no | Additional data that can be used for identifying, managing, or monitoring a message. Data included here will also be automatically included in the message Delivery Report. The maximum value is 4000 characters. |
| `options` | object | no | Options applicable to all messages in the request. |
| `options.schedule` | object | no | Options for scheduling a message. |
| `options.schedule.bulkId` | string | no | Unique ID assigned to the request if messaging multiple recipients or sending multiple messages via a single API request. If not provided, it will be auto-generated and returned in the API response. |
| `options.schedule.sendAt` | date | no | Date and time when the message is to be sent. Used for scheduled messages. Has the following format: `yyyy-MM-dd'T'HH:mm:ss.SSSZ`, and can only be scheduled for no later than 180 days in advance. |
| `options.schedule.sendingSpeedLimit` | object | no | Limits the send speed when sending messages in bulk to deliver messages over a longer period of time. You may wish to use this to allow your systems or agents to handle large amounts of incoming traffic, e.g., if you are expecting recipients to follow through with a call-to-action option from a message you sent. Not setting a send speed limit can overwhelm your resources with incoming traffic. |
| `options.schedule.sendingSpeedLimit.amount` | number | no | The number of messages to be sent per timeUnit. By default, the system sends messages as fast as the infrastructure allows. Use this parameter to adapt sending capacity to your needs. The system is only able to work against its maximum capacity for ambitious message batches. |
| `options.schedule.sendingSpeedLimit.timeUnit` | string | no | The time unit to define when setting a messaging speed limit. Defaults to `MINUTE`. |
| `options.tracking` | object | no | Sets up [URL shortening](https://www.infobip.com/docs/url-shortening) and tracking feature. |
| `options.tracking.shortenUrl` | boolean | no | Enable shortening of the URLs within a message. Set this to `true`, if you want to set up other URL options. |
| `options.tracking.trackClicks` | boolean | no | Enable tracking of short URL clicks within a message: which URL was clicked, how many times, and by whom. |
| `options.tracking.trackingUrl` | string | no | The URL of your callback server on to which the Click report will be sent. |
| `options.tracking.removeProtocol` | boolean | no | Remove a protocol, such as `https://`, from links to shorten a message. Note that some mobiles may not recognize such links as a URL. |
| `options.tracking.customDomain` | string | no | Select a predefined custom domain to use when generating a short URL. |
| `options.includeSmsCountInResponse` | boolean | no | Set to true to return `messageCount` in the response. The `messageCount` is the total count of SMS submitted in the request. SMS messages have a character limit and messages longer than the limit will be split into multiple SMS. Not compatible with `binary` message content type. |
| `options.conversionTracking` | object | no | Allows you to set up tracking parameters to track conversion metrics. For more details, see: [SMS with conversion tracking](https://www.infobip.com/docs/sms/sms-over-api#send-sms-with-conversion-tracking). |
| `options.conversionTracking.useConversionTracking` | boolean | no | Indicates if a message has to be tracked for conversion rates. Default "false". |
| `options.conversionTracking.conversionTrackingName` | string | no | Sets a custom conversion type naming convention, e.g. `ONE_TIME_PIN` or `SOCIAL_INVITES`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bulkId": "string",
      "messages": {
        "destination": "string",
        "details": {
          "messageCount": 1
        },
        "messageId": "string",
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
| `bulkId` | string |  |
| `messages` | array<object> |  |
| `messages.destination` | string |  |
| `messages.details` | object |  |
| `messages.details.messageCount` | number |  |
| `messages.messageId` | string |  |
| `messages.status` | object |  |
| `messages.status.action` | string |  |
| `messages.status.description` | string |  |
| `messages.status.groupId` | number |  |
| `messages.status.groupName` | string |  |
| `messages.status.id` | number |  |
| `messages.status.name` | string |  |

## Native endpoint

Through the native Infobip API, this operation is `POST /sms/3/messages` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms-message.md) for the provider-specific parameters and requirements.

