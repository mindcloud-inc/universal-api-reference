# Mailchimp: Create Campaign

Creates a new campaign in Mailchimp.

```
POST https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "absplit",
  "recipients.list_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "absplit",
    "recipients.list_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content_type` | string | no |  |
| `rss_opts` | object | no |  |
| `social_card` | object | no |  |
| `tracking` | object | no |  |
| `type` | list<string> | yes | Campaign type. One of: `absplit`, `plaintext`, `regular`, `rss`, `variate`. |
| `variate_settings` | object | no |  |
| `recipients` | object | no | Campaign recipients object. |
| `settings` | object | no | Campaign settings object. |
| `recipients.list_id` | string | yes | The unique audience (list) id for campaign recipients. |
| `settings.subject_line` | string | no | Campaign email subject line. |
| `settings.title` | string | no | Internal campaign title. |
| `settings.from_name` | string | no | From name used in campaign emails. |
| `settings.reply_to` | string | no | Reply-to email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archiveUrl": "https://example.com",
      "contentType": "string",
      "createTime": "string",
      "deliveryStatus": {
        "enabled": true
      },
      "emailsSent": 1,
      "id": "string",
      "links": [
        [
          {}
        ]
      ],
      "longArchiveUrl": "https://example.com",
      "needsBlockRefresh": true,
      "recipients": {
        "listId": "string",
        "listIsActive": true,
        "listName": "Ava Chen",
        "recipientCount": 1,
        "segmentText": "string"
      },
      "resendable": true,
      "sendTime": "string",
      "settings": {
        "authenticate": true,
        "autoFooter": true,
        "autoTweet": true,
        "dragAndDrop": true,
        "fbComments": true,
        "folderId": "string",
        "inlineCss": true,
        "templateId": 1,
        "timewarp": true,
        "title": "string",
        "toName": "Ava Chen",
        "useConversation": true
      },
      "status": "string",
      "tracking": {
        "clicktale": "string",
        "ecomm360": true,
        "goalTracking": true,
        "googleAnalytics": "string",
        "htmlClicks": true,
        "opens": true,
        "textClicks": true
      },
      "type": "string",
      "webId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archiveUrl` | string |  |
| `contentType` | string |  |
| `createTime` | string |  |
| `deliveryStatus` | object |  |
| `deliveryStatus.enabled` | boolean |  |
| `emailsSent` | number |  |
| `id` | string |  |
| `links[]` | array<object> |  |
| `links[].href` | string |  |
| `links[].method` | string |  |
| `links[].rel` | string |  |
| `links[].schema` | string |  |
| `links[].targetSchema` | string |  |
| `longArchiveUrl` | string |  |
| `needsBlockRefresh` | boolean |  |
| `recipients` | object |  |
| `recipients.listId` | string |  |
| `recipients.listIsActive` | boolean |  |
| `recipients.listName` | string |  |
| `recipients.recipientCount` | number |  |
| `recipients.segmentText` | string |  |
| `resendable` | boolean |  |
| `sendTime` | string |  |
| `settings` | object |  |
| `settings.authenticate` | boolean |  |
| `settings.autoFooter` | boolean |  |
| `settings.autoTweet` | boolean |  |
| `settings.dragAndDrop` | boolean |  |
| `settings.fbComments` | boolean |  |
| `settings.folderId` | string |  |
| `settings.inlineCss` | boolean |  |
| `settings.templateId` | number |  |
| `settings.timewarp` | boolean |  |
| `settings.title` | string |  |
| `settings.toName` | string |  |
| `settings.useConversation` | boolean |  |
| `status` | string |  |
| `tracking` | object |  |
| `tracking.clicktale` | string |  |
| `tracking.ecomm360` | boolean |  |
| `tracking.goalTracking` | boolean |  |
| `tracking.googleAnalytics` | string |  |
| `tracking.htmlClicks` | boolean |  |
| `tracking.opens` | boolean |  |
| `tracking.textClicks` | boolean |  |
| `type` | string |  |
| `webId` | number |  |

## Native endpoint

Through the native Mailchimp API, this operation is `POST campaigns` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

