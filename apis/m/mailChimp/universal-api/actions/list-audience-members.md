# Mailchimp: List Audience Members

Retrieves members from a Mailchimp audience.

```
GET https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-audience-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-audience-members?connectionId=$CONNECTION_ID&limit=25&offset=0&list_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "list_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-audience-members?${params}`, {
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
| `before_last_changed` | string | no |  |
| `before_timestamp_opt` | string | no |  |
| `email_type` | string | no |  |
| `exclude_fields` | string | no |  |
| `fields` | string | no |  |
| `interest_category_id` | string | no |  |
| `interest_ids` | string | no |  |
| `interest_match` | string | no |  |
| `list_id` | string | yes | The unique ID for the Mailchimp audience. |
| `since_last_campaign` | boolean | no |  |
| `since_last_changed` | string | no |  |
| `since_timestamp_opt` | string | no |  |
| `status` | string | no |  |
| `unique_email_id` | string | no |  |
| `unsubscribed_since` | string | no |  |
| `vip_only` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": [
        [
          {}
        ]
      ],
      "listId": "string",
      "members": [
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
| `links[]` | array<object> |  |
| `links[].href` | string |  |
| `links[].method` | string |  |
| `links[].rel` | string |  |
| `links[].schema` | string |  |
| `links[].targetSchema` | string |  |
| `listId` | string |  |
| `members[]` | array<object> |  |
| `members[].consentsToOneToOneMessaging` | boolean |  |
| `members[].contactId` | string |  |
| `members[].emailAddress` | string |  |
| `members[].emailClient` | string |  |
| `members[].emailType` | string |  |
| `members[].fullName` | string |  |
| `members[].id` | string |  |
| `members[].ipOpt` | string |  |
| `members[].ipSignup` | string |  |
| `members[].language` | string |  |
| `members[].lastChanged` | string |  |
| `members[].links[]` | array<object> |  |
| `members[].links[].href` | string |  |
| `members[].links[].method` | string |  |
| `members[].links[].rel` | string |  |
| `members[].links[].targetSchema` | string |  |
| `members[].listId` | string |  |
| `members[].location` | object |  |
| `members[].location.countryCode` | string |  |
| `members[].location.dstoff` | number |  |
| `members[].location.gmtoff` | number |  |
| `members[].location.latitude` | number |  |
| `members[].location.longitude` | number |  |
| `members[].location.region` | string |  |
| `members[].location.timezone` | string |  |
| `members[].memberRating` | number |  |
| `members[].mergeFields` | object |  |
| `members[].mergeFields.aDDRESS` | object |  |
| `members[].mergeFields.aDDRESS.addr1` | string |  |
| `members[].mergeFields.aDDRESS.addr2` | string |  |
| `members[].mergeFields.aDDRESS.city` | string |  |
| `members[].mergeFields.aDDRESS.country` | string |  |
| `members[].mergeFields.aDDRESS.state` | string |  |
| `members[].mergeFields.aDDRESS.zip` | string |  |
| `members[].mergeFields.bIRTHDAY` | string |  |
| `members[].mergeFields.cOMPANY` | string |  |
| `members[].mergeFields.fNAME` | string |  |
| `members[].mergeFields.lNAME` | string |  |
| `members[].mergeFields.pHONE` | string |  |
| `members[].smsPhoneNumber` | string |  |
| `members[].smsSubscriptionLastUpdated` | string |  |
| `members[].smsSubscriptionStatus` | string |  |
| `members[].source` | string |  |
| `members[].stats` | object |  |
| `members[].stats.avgClickRate` | number |  |
| `members[].stats.avgOpenRate` | number |  |
| `members[].status` | string |  |
| `members[].tags[]` | array<string> |  |
| `members[].tagsCount` | number |  |
| `members[].timestampOpt` | string |  |
| `members[].timestampSignup` | string |  |
| `members[].uniqueEmailId` | string |  |
| `members[].vip` | boolean |  |
| `members[].webId` | number |  |
| `totalItems` | number |  |

## Native endpoint

Through the native Mailchimp API, this operation is `GET lists/:list_id/members` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-audience-members.md) for the provider-specific parameters and requirements.

