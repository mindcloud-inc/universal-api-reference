# Infobip: Send Email Messages



```
POST https://connect.mindcloud.co/v1/universal/infobip/latest/actions/send-email-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/send-email-messages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messages": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infobip/latest/actions/send-email-messages', {
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
| `messages.sender` | string | no | Email address with optional sender name. Note: This field is required if `templateId` is not present. |
| `messages.destinations` | list<object> | no | An array of destination objects for where messages are being sent. A valid destination is required. Note: Maximum number of recipients is 1000 overall including `to`, `cc` and `bcc` field. |
| `messages.content` | object | no | Message content. |
| `messages.content.subject` | string | no | Message subject. Note: This field is required if `templateId` is not present. |
| `messages.content.text` | string | no | Body of the message. |
| `messages.content.html` | string | no | The message's body in HTML format. If both `html` and `text` fields are included, the `text` field will be disregarded, and the message will be sent using the `html` content. |
| `messages.content.ampHtml` | string | no | The message's body in AMP HTML format. If you include `ampHtml`, you must also include `html`, which will be displayed if AMP is not supported. Keep in mind that not all email clients support AMP HTML. For guidance on configuring the Gmail client, please visit this link: https://developers.google.com/gmail/ampemail/ . |
| `messages.content.templateId` | string | no | The Template ID with predefined email content created through the Infobip web interface or API. When `templateId` is specified, the `html` and `text` fields will be disregarded. Note: `templateId` only supports the `Broadcast` value; `Content` and `Flow` templates are not supported. |
| `messages.content.attachments` | list<object> | no | File attachments. |
| `messages.content.inlineImages` | list<object> | no | Allows for inserting an image file inside the HTML code of the email by using `cid:FILENAME` instead of providing an external link to the image. |
| `messages.content.defaultPlaceholders` | string | no | General placeholders: `{"ph1": "Success"}` will replace the key `{{ph1}}` with the value Success throughout the email, including the `subject`, `text`, and HTML. If there are multiple recipients in the To field, this placeholder will use the same value for the key ph1 for all recipients. |
| `messages.content.landingPagePlaceholders` | string | no | Personalize Opt-Out Landing Page by inserting placeholders. Insert placeholder or tag while designing landing page. Value should be defined as: `{"unsubscribe": "Unsubscribe"}` |
| `messages.content.optoutLandingPageId` | string | no | The Opt-Out Landing Page ID specifies the page to be displayed when an end user clicks the unsubscribe link. If the ID is not provided, the default opt-out landing page will be used. Create a landing page over Infobip web interface and use its ID, for example, `1_23456.` |
| `messages.content.templateLanguageVersion` | string | no | Indicates the version of the template language to be used in the current message template. Use version 1 for the older template language and version 2 to access features of the new template language. If not specified, version 1 will be used by default. |
| `messages.content.headers` | string | no | Additional email headers for customization that can be provided in a form of JSON. Example: `headers={"X-CustomHeader": "Header value"}`. There are a few exceptions of headers which are not adjustable through this option: `To`, `Cc`, `Bcc`, `From`, `Subject`, `Content-Type`, `DKIM-Signature`, `Content-Transfer-Encoding`, `Return-Path`, `MIME-Version` |
| `messages.options` | object | no | Message options. |
| `messages.options.platform` | object | no | Platform options. For more details, see [documentation](https://www.infobip.com/docs/cpaas-x/application-and-entity-management). |
| `messages.options.validityPeriod` | object | no | Message validity period. Once expired, the message won't be sent. Validity period longer than 48h is not supported. If exceeded, it will be automatically set to 48h. |
| `messages.options.deliveryTimeWindow` | object | no | Sets specific message delivery window outside of which messages won't be delivered. Often, used when there are restrictions on when messages can be sent. The exact time of the day to start sending messages can be defined using the `from` property. The exact time of the day to end sending messages can be defined using the `to` property. Properties `from` and `to` should be both provided with the minimum 1 hour difference or omitted. |
| `messages.options.campaignReferenceId` | string | no | ID that allows you to track, analyze, and show an aggregated overview and the performance of individual campaigns per sending channel. |
| `messages.webhooks` | object | no | Provides options for configuring message webhooks. |
| `messages.webhooks.delivery` | object | no | Provides options for configuring the delivery report behavior. |
| `messages.webhooks.contentType` | string | no | Preferred delivery report content type, `application/json` or `application/xml`. |
| `messages.webhooks.callbackData` | string | no | Additional data that can be used for identifying, managing, or monitoring a message. Data included here will also be automatically included in the message Delivery Report. The maximum value is 4000 characters. |
| `messages.ips` | object | no | IP options per message. |
| `messages.ips.ipPoolId` | string | no | The ID of the IP pool that will be used to send the email. |
| `messages.placeholdersMasking` | list<object> | no | Options to full or partially mask placeholders. |
| `messages.storage` | object | no | [Email storage options](https://www.infobip.com/docs/email/email-storage-and-retrieval) per message. |
| `messages.storage.skipPassive` | boolean | no | Set to true to skip [passive email storage](https://www.infobip.com/docs/email/email-storage-and-retrieval/passive-email-storage) (long-term storage used for compliance, legal, or audit purposes). If `false` or not set, the account-level setting is used. |
| `messages.storage.skipActive` | boolean | no | Set to true to skip [active email storage](https://www.infobip.com/docs/email/email-storage-and-retrieval/active-email-storage) (short-term storage used for troubleshooting or support). If `false` or not set, the account-level setting is used. |
| `options` | object | no | Options applicable to all messages in the request. |
| `options.schedule` | object | no | Options for scheduling a message. |
| `options.schedule.bulkId` | string | no | Unique ID assigned to the request if messaging multiple recipients or sending multiple messages via a single API request. If not provided, it will be auto-generated and returned in the API response. |
| `options.schedule.sendAt` | string | no | Date and time when the message is to be sent. Used for scheduled messages. Has the following format: `yyyy-MM-dd'T'HH:mm:ss.SSSZ`, and can only be scheduled for no later than 5 days in advance. |
| `options.tracking` | object | no | Sets up [URL shortening](https://www.infobip.com/docs/url-shortening) and tracking feature. |
| `options.tracking.track` | boolean | no | Enable or disable open and click tracking. Passing true will only enable tracking and the statistics will be visible in the web interface alone. This can be explicitly overridden by `trackClicks` and `trackOpens`. |
| `options.tracking.trackOpens` | boolean | no | This parameter enables or disables track open feature. |
| `options.tracking.trackClicks` | boolean | no | This parameter enables or disables track click feature. |
| `options.tracking.trackingUrl` | string | no | The URL on your callback server on which the open and click notifications will be sent. See [Tracking Notifications](https://www.infobip.com/docs/email/send-email-over-api#tracking-notifications) for details. |
| `options.tracking.trackingPixelPosition` | string | no | This parameter specifies the position of the open tracking pixel within the email content. Allowed values are `TOP` and `BOTTOM`. If no value is provided, the default is `TOP`. |
| `options.clientPriority` | string | no | Client priority set on request. Must be 'HIGH', 'STANDARD' or 'LOW'. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bulkId": "string",
      "messages": {
        "destination": "string",
        "details": {},
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
| `messages.messageId` | string |  |
| `messages.status` | object |  |
| `messages.status.action` | string |  |
| `messages.status.description` | string |  |
| `messages.status.groupId` | number |  |
| `messages.status.groupName` | string |  |
| `messages.status.id` | number |  |
| `messages.status.name` | string |  |

## Native endpoint

Through the native Infobip API, this operation is `POST /email/4/messages` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-email-messages.md) for the provider-specific parameters and requirements.

