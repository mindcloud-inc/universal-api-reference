# ActiveCampaign: List Lists

Retrieves lists from ActiveCampaign.

```
GET https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/list-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveCampaign `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/list-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/list-lists?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "activeSubscribers": "string",
      "analyticsDomains": {},
      "analyticsSource": "string",
      "analyticsUa": "string",
      "carboncopy": "string",
      "cdate": "2026-05-07T12:00:00.000Z",
      "channel": "string",
      "createdBy": {},
      "createdTimestamp": "2026-05-07T12:00:00.000Z",
      "deletestamp": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "facebookSession": {},
      "fulladdress": "string",
      "getUnsubscribeReason": "string",
      "id": "string",
      "links": {
        "addressLists": "https://example.com",
        "contactGoalLists": "https://example.com",
        "user": "https://example.com"
      },
      "name": "Ava Chen",
      "nonDeletedSubscribers": "string",
      "optinmessageid": "string",
      "optinoptout": "string",
      "optoutconf": "string",
      "pEmbedImage": "string",
      "private": "string",
      "pUseAnalyticsLink": "https://example.com",
      "pUseAnalyticsRead": "string",
      "pUseCaptcha": "string",
      "pUseFacebook": "string",
      "pUseTracking": "string",
      "pUseTwitter": "string",
      "requireName": "Ava Chen",
      "senderAddr1": "string",
      "senderAddr2": "string",
      "senderCity": "string",
      "senderCountry": "string",
      "senderName": "Ava Chen",
      "senderPhone": "string",
      "senderReminder": "string",
      "senderState": "string",
      "senderUrl": "https://example.com",
      "senderZip": "string",
      "sendLastBroadcast": "string",
      "stringid": "string",
      "subscriptionNotify": "string",
      "toName": "Ava Chen",
      "twitterToken": "string",
      "twitterTokenSecret": "string",
      "udate": "2026-05-07T12:00:00.000Z",
      "unsubscriptionNotify": "string",
      "updatedBy": {},
      "updatedTimestamp": "2026-05-07T12:00:00.000Z",
      "user": "string",
      "userid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeSubscribers` | string |  |
| `analyticsDomains` | object |  |
| `analyticsSource` | string |  |
| `analyticsUa` | string |  |
| `carboncopy` | string |  |
| `cdate` | date |  |
| `channel` | string |  |
| `createdBy` | object |  |
| `createdTimestamp` | date |  |
| `deletestamp` | date |  |
| `description` | string |  |
| `facebookSession` | object |  |
| `fulladdress` | string |  |
| `getUnsubscribeReason` | string |  |
| `id` | string |  |
| `links.addressLists` | string |  |
| `links.contactGoalLists` | string |  |
| `links.user` | string |  |
| `name` | string |  |
| `nonDeletedSubscribers` | string |  |
| `optinmessageid` | string |  |
| `optinoptout` | string |  |
| `optoutconf` | string |  |
| `pEmbedImage` | string |  |
| `private` | string |  |
| `pUseAnalyticsLink` | string |  |
| `pUseAnalyticsRead` | string |  |
| `pUseCaptcha` | string |  |
| `pUseFacebook` | string |  |
| `pUseTracking` | string |  |
| `pUseTwitter` | string |  |
| `requireName` | string |  |
| `senderAddr1` | string |  |
| `senderAddr2` | string |  |
| `senderCity` | string |  |
| `senderCountry` | string |  |
| `senderName` | string |  |
| `senderPhone` | string |  |
| `senderReminder` | string |  |
| `senderState` | string |  |
| `senderUrl` | string |  |
| `senderZip` | string |  |
| `sendLastBroadcast` | string |  |
| `stringid` | string |  |
| `subscriptionNotify` | string |  |
| `toName` | string |  |
| `twitterToken` | string |  |
| `twitterTokenSecret` | string |  |
| `udate` | date |  |
| `unsubscriptionNotify` | string |  |
| `updatedBy` | object |  |
| `updatedTimestamp` | date |  |
| `user` | string |  |
| `userid` | string |  |

## Native endpoint

Through the native ActiveCampaign API, this operation is `GET /lists` (base URL `{{credentials.apiUrl}}/api/3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-lists.md) for the provider-specific parameters and requirements.

