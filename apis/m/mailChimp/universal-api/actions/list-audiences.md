# Mailchimp: List Audiences

Retrieves audiences from Mailchimp.

```
GET https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-audiences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-audiences?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-audiences?${params}`, {
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
| `fields` | string | no | Comma-separated fields to include in the response. Accepts multiple values as an array. |
| `excludeFields` | string | no | Comma-separated fields to exclude from the response. |
| `beforeDateCreated` | date | no | Return audiences created before this ISO-8601 datetime. |
| `sinceDateCreated` | date | no | Return audiences created after this ISO-8601 datetime. |
| `beforeCampaignLastSent` | date | no | Return audiences with last campaign sent before this ISO-8601 datetime. |
| `sinceCampaignLastSent` | date | no | Return audiences with last campaign sent after this ISO-8601 datetime. |
| `email` | string | no | Restrict results to audiences containing this subscriber email. |
| `hasEcommerceStore` | boolean | no | Only include audiences connected to an active ecommerce store. |
| `includeTotalContacts` | boolean | no | Include approximate total contact counts in stats. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "constraints": {
        "currentTotalInstances": 1,
        "maxInstances": 1,
        "mayCreate": true
      },
      "links": [
        [
          {}
        ]
      ],
      "lists": [
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
| `constraints` | object |  |
| `constraints.currentTotalInstances` | number |  |
| `constraints.maxInstances` | number |  |
| `constraints.mayCreate` | boolean |  |
| `links[]` | array<object> |  |
| `links[].href` | string |  |
| `links[].method` | string |  |
| `links[].rel` | string |  |
| `links[].schema` | string |  |
| `links[].targetSchema` | string |  |
| `lists[]` | array<object> |  |
| `lists[].beamerAddress` | string |  |
| `lists[].campaignDefaults` | object |  |
| `lists[].campaignDefaults.fromEmail` | string |  |
| `lists[].campaignDefaults.fromName` | string |  |
| `lists[].campaignDefaults.language` | string |  |
| `lists[].campaignDefaults.subject` | string |  |
| `lists[].contact` | object |  |
| `lists[].contact.address1` | string |  |
| `lists[].contact.address2` | string |  |
| `lists[].contact.city` | string |  |
| `lists[].contact.company` | string |  |
| `lists[].contact.country` | string |  |
| `lists[].contact.phone` | string |  |
| `lists[].contact.state` | string |  |
| `lists[].contact.zip` | string |  |
| `lists[].dateCreated` | string |  |
| `lists[].doubleOptin` | boolean |  |
| `lists[].emailTypeOption` | boolean |  |
| `lists[].hasWelcome` | boolean |  |
| `lists[].id` | string |  |
| `lists[].links[]` | array<object> |  |
| `lists[].links[].href` | string |  |
| `lists[].links[].method` | string |  |
| `lists[].links[].rel` | string |  |
| `lists[].links[].targetSchema` | string |  |
| `lists[].listRating` | number |  |
| `lists[].marketingPermissions` | boolean |  |
| `lists[].modules[]` | array<string> |  |
| `lists[].name` | string |  |
| `lists[].notifyOnSubscribe` | string |  |
| `lists[].notifyOnUnsubscribe` | string |  |
| `lists[].permissionReminder` | string |  |
| `lists[].stats` | object |  |
| `lists[].stats.avgSubRate` | number |  |
| `lists[].stats.avgUnsubRate` | number |  |
| `lists[].stats.campaignCount` | number |  |
| `lists[].stats.campaignLastSent` | string |  |
| `lists[].stats.cleanedCount` | number |  |
| `lists[].stats.cleanedCountSinceSend` | number |  |
| `lists[].stats.clickRate` | number |  |
| `lists[].stats.lastSubDate` | string |  |
| `lists[].stats.lastUnsubDate` | string |  |
| `lists[].stats.memberCount` | number |  |
| `lists[].stats.memberCountSinceSend` | number |  |
| `lists[].stats.mergeFieldCount` | number |  |
| `lists[].stats.openRate` | number |  |
| `lists[].stats.targetSubRate` | number |  |
| `lists[].stats.unsubscribeCount` | number |  |
| `lists[].stats.unsubscribeCountSinceSend` | number |  |
| `lists[].subscribeUrlLong` | string |  |
| `lists[].subscribeUrlShort` | string |  |
| `lists[].useArchiveBar` | boolean |  |
| `lists[].visibility` | string |  |
| `lists[].webId` | number |  |
| `totalItems` | number |  |

## Native endpoint

Through the native Mailchimp API, this operation is `GET lists` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-audiences.md) for the provider-specific parameters and requirements.

