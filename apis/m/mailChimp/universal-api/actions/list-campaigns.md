# Mailchimp: List Campaigns

Retrieves campaigns from Mailchimp.

```
GET https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-campaigns?${params}`, {
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
| `before_create_time` | date | no | Only include campaigns created before this ISO 8601 datetime. |
| `before_send_time` | date | no | Only include campaigns sent before this ISO 8601 datetime. |
| `exclude_fields` | string | no |  |
| `fields` | string | no |  |
| `folder_id` | string | no | Filter campaigns by folder id. |
| `include_resend_shortcut_eligibility` | boolean | no | Include resend shortcut eligibility in campaign response. |
| `list_id` | string | no | Filter campaigns by audience/list id. |
| `member_id` | string | no | Filter campaigns sent to a specific member hash. |
| `since_create_time` | date | no | Only include campaigns created after this ISO 8601 datetime. |
| `since_send_time` | date | no | Only include campaigns sent after this ISO 8601 datetime. |
| `status` | list<string> | no | Filter campaigns by status. One of: `paused`, `save`, `schedule`, `sending`, `sent`. |
| `type` | list<string> | no | Filter campaigns by type. One of: `absplit`, `plaintext`, `regular`, `rss`, `variate`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaigns": [
        [
          {}
        ]
      ],
      "links": [
        [
          {}
        ]
      ],
      "totalItems": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaigns[]` | array<object> |  |
| `campaigns[].archiveUrl` | string |  |
| `campaigns[].contentType` | string |  |
| `campaigns[].createTime` | string |  |
| `campaigns[].deliveryStatus` | object |  |
| `campaigns[].deliveryStatus.enabled` | boolean |  |
| `campaigns[].emailsSent` | number |  |
| `campaigns[].id` | string |  |
| `campaigns[].links[]` | array<object> |  |
| `campaigns[].links[].href` | string |  |
| `campaigns[].links[].method` | string |  |
| `campaigns[].links[].rel` | string |  |
| `campaigns[].links[].schema` | string |  |
| `campaigns[].links[].targetSchema` | string |  |
| `campaigns[].longArchiveUrl` | string |  |
| `campaigns[].needsBlockRefresh` | boolean |  |
| `campaigns[].recipients` | object |  |
| `campaigns[].recipients.listId` | string |  |
| `campaigns[].recipients.listIsActive` | boolean |  |
| `campaigns[].recipients.listName` | string |  |
| `campaigns[].recipients.recipientCount` | number |  |
| `campaigns[].recipients.segmentText` | string |  |
| `campaigns[].resendable` | boolean |  |
| `campaigns[].sendTime` | string |  |
| `campaigns[].settings` | object |  |
| `campaigns[].settings.authenticate` | boolean |  |
| `campaigns[].settings.autoFooter` | boolean |  |
| `campaigns[].settings.autoTweet` | boolean |  |
| `campaigns[].settings.dragAndDrop` | boolean |  |
| `campaigns[].settings.fbComments` | boolean |  |
| `campaigns[].settings.folderId` | string |  |
| `campaigns[].settings.inlineCss` | boolean |  |
| `campaigns[].settings.templateId` | number |  |
| `campaigns[].settings.timewarp` | boolean |  |
| `campaigns[].settings.title` | string |  |
| `campaigns[].settings.toName` | string |  |
| `campaigns[].settings.useConversation` | boolean |  |
| `campaigns[].status` | string |  |
| `campaigns[].tracking` | object |  |
| `campaigns[].tracking.clicktale` | string |  |
| `campaigns[].tracking.ecomm360` | boolean |  |
| `campaigns[].tracking.goalTracking` | boolean |  |
| `campaigns[].tracking.googleAnalytics` | string |  |
| `campaigns[].tracking.htmlClicks` | boolean |  |
| `campaigns[].tracking.opens` | boolean |  |
| `campaigns[].tracking.textClicks` | boolean |  |
| `campaigns[].type` | string |  |
| `campaigns[].webId` | number |  |
| `links[]` | array<object> |  |
| `links[].href` | string |  |
| `links[].method` | string |  |
| `links[].rel` | string |  |
| `links[].schema` | string |  |
| `links[].targetSchema` | string |  |
| `totalItems` | number |  |

## Native endpoint

Through the native Mailchimp API, this operation is `GET campaigns` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

