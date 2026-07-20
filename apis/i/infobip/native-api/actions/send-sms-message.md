# Send SMS Message with Infobip

## Endpoint

- **Method:** `POST`
- **Path:** `/sms/3/messages`
- **Base URL:** `https://rkpzwe.api.infobip.com`
- **Official documentation:** [Send SMS Message](https://www.infobip.com/docs/api/channels/sms/outbound-sms/send-sms-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages` | body | `list<object>` | yes | An array of message objects of a single message or multiple messages sent under one bulk ID. |
| `messages.sender` | body | `string` | no | The sender ID. It can be alphanumeric or numeric (e.g., `CompanyName`). Make sure you don't exceed [character limit](https://www.infobip.com/docs/sms/get-started#sender-names). |
| `messages.destinations` | body | `list<object>` | no | An array of destination objects for where messages are being sent. A valid destination is required. |
| `messages.content` | body | `object` | no | Message content. |
| `messages.options` | body | `object` | no | Message options. |
| `messages.options.platform` | body | `object` | no | Platform options. For more details, see [documentation](https://www.infobip.com/docs/cpaas-x/application-and-entity-management). |
| `messages.options.validityPeriod` | body | `object` | no | Message validity period. Once expired, the message won't be sent. Validity period longer than 48h is not supported. If exceeded, it will be automatically set to 48h. |
| `messages.options.deliveryTimeWindow` | body | `object` | no | Sets specific message delivery window outside of which messages won't be delivered. Often, used when there are restrictions on when messages can be sent. The exact time of the day to start sending messages can be defined using the `from` property. The exact time of the day to end sending messages can be defined using the `to` property. Properties `from` and `to` should be both provided with the minimum 1 hour difference or omitted. |
| `messages.options.campaignReferenceId` | body | `string` | no | ID that allows you to track, analyze, and show an aggregated overview and the performance of individual campaigns per sending channel. |
| `messages.options.regional` | body | `object` | no | Region-specific parameters, often imposed by local laws. Use this, if country or region that you are sending an SMS to requires additional information. |
| `messages.options.flash` | body | `boolean` | no | Allows for sending a [flash SMS](https://www.infobip.com/docs/sms/message-types#flash-sms) to automatically appear on recipient devices without interaction. Set to `true` to enable flash SMS, or leave the default value, `false` to send a standard SMS. |
| `messages.webhooks` | body | `object` | no | Provides options for configuring message webhooks. |
| `messages.webhooks.delivery` | body | `object` | no | Provides options for configuring the delivery report behavior. |
| `messages.webhooks.contentType` | body | `string` | no | Preferred delivery report content type, `application/json` or `application/xml`. |
| `messages.webhooks.callbackData` | body | `string` | no | Additional data that can be used for identifying, managing, or monitoring a message. Data included here will also be automatically included in the message Delivery Report. The maximum value is 4000 characters. |
| `options` | body | `object` | no | Options applicable to all messages in the request. |
| `options.schedule` | body | `object` | no | Options for scheduling a message. |
| `options.schedule.bulkId` | body | `string` | no | Unique ID assigned to the request if messaging multiple recipients or sending multiple messages via a single API request. If not provided, it will be auto-generated and returned in the API response. |
| `options.schedule.sendAt` | body | `date` | no | Date and time when the message is to be sent. Used for scheduled messages. Has the following format: `yyyy-MM-dd'T'HH:mm:ss.SSSZ`, and can only be scheduled for no later than 180 days in advance. |
| `options.schedule.sendingSpeedLimit` | body | `object` | no | Limits the send speed when sending messages in bulk to deliver messages over a longer period of time. You may wish to use this to allow your systems or agents to handle large amounts of incoming traffic, e.g., if you are expecting recipients to follow through with a call-to-action option from a message you sent. Not setting a send speed limit can overwhelm your resources with incoming traffic. |
| `options.schedule.sendingSpeedLimit.amount` | body | `number` | no | The number of messages to be sent per timeUnit. By default, the system sends messages as fast as the infrastructure allows. Use this parameter to adapt sending capacity to your needs. The system is only able to work against its maximum capacity for ambitious message batches. |
| `options.schedule.sendingSpeedLimit.timeUnit` | body | `string` | no | The time unit to define when setting a messaging speed limit. Defaults to `MINUTE`. |
| `options.tracking` | body | `object` | no | Sets up [URL shortening](https://www.infobip.com/docs/url-shortening) and tracking feature. |
| `options.tracking.shortenUrl` | body | `boolean` | no | Enable shortening of the URLs within a message. Set this to `true`, if you want to set up other URL options. |
| `options.tracking.trackClicks` | body | `boolean` | no | Enable tracking of short URL clicks within a message: which URL was clicked, how many times, and by whom. |
| `options.tracking.trackingUrl` | body | `string` | no | The URL of your callback server on to which the Click report will be sent. |
| `options.tracking.removeProtocol` | body | `boolean` | no | Remove a protocol, such as `https://`, from links to shorten a message. Note that some mobiles may not recognize such links as a URL. |
| `options.tracking.customDomain` | body | `string` | no | Select a predefined custom domain to use when generating a short URL. |
| `options.includeSmsCountInResponse` | body | `boolean` | no | Set to true to return `messageCount` in the response. The `messageCount` is the total count of SMS submitted in the request. SMS messages have a character limit and messages longer than the limit will be split into multiple SMS. Not compatible with `binary` message content type. |
| `options.conversionTracking` | body | `object` | no | Allows you to set up tracking parameters to track conversion metrics. For more details, see: [SMS with conversion tracking](https://www.infobip.com/docs/sms/sms-over-api#send-sms-with-conversion-tracking). |
| `options.conversionTracking.useConversionTracking` | body | `boolean` | no | Indicates if a message has to be tracked for conversion rates. Default "false". |
| `options.conversionTracking.conversionTrackingName` | body | `string` | no | Sets a custom conversion type naming convention, e.g. `ONE_TIME_PIN` or `SOCIAL_INVITES`. |
