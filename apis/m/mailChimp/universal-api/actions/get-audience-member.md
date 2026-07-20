# Mailchimp: Get Audience Member

Retrieves a member from a Mailchimp audience.

```
GET https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-audience-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-audience-member?connectionId=$CONNECTION_ID&list_id=string&subscriber_hash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "list_id": "string",
  "subscriber_hash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-audience-member?${params}`, {
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
| `exclude_fields` | string | no |  |
| `fields` | string | no |  |
| `list_id` | string | yes | The unique ID for the Mailchimp audience. |
| `subscriber_hash` | string | yes | MD5 hash of the lowercase subscriber email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "consentsToOneToOneMessaging": true,
      "contactId": "string",
      "emailAddress": "ava@example.com",
      "emailClient": "ava@example.com",
      "emailType": "ava@example.com",
      "fullName": "Ava Chen",
      "id": "string",
      "ipOpt": "string",
      "ipSignup": "string",
      "language": "string",
      "lastChanged": "string",
      "links": [
        [
          {}
        ]
      ],
      "listId": "string",
      "location": {
        "countryCode": "string",
        "dstoff": 1,
        "gmtoff": 1,
        "latitude": 1,
        "longitude": 1,
        "region": "string",
        "timezone": "string"
      },
      "memberRating": 1,
      "mergeFields": {
        "aDDRESS": {
          "addr1": "string",
          "addr2": "string",
          "city": "string",
          "country": "string",
          "state": "string",
          "zip": "string"
        },
        "bIRTHDAY": "string",
        "cOMPANY": "string",
        "fNAME": "Ava Chen",
        "lNAME": "Ava Chen",
        "pHONE": "string"
      },
      "smsPhoneNumber": "string",
      "smsSubscriptionLastUpdated": "string",
      "smsSubscriptionStatus": "string",
      "source": "string",
      "stats": {
        "avgClickRate": 1,
        "avgOpenRate": 1
      },
      "status": "string",
      "tags": [
        [
          "string"
        ]
      ],
      "tagsCount": 1,
      "timestampOpt": "string",
      "timestampSignup": "string",
      "uniqueEmailId": "ava@example.com",
      "vip": true,
      "webId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `consentsToOneToOneMessaging` | boolean |  |
| `contactId` | string |  |
| `emailAddress` | string |  |
| `emailClient` | string |  |
| `emailType` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `ipOpt` | string |  |
| `ipSignup` | string |  |
| `language` | string |  |
| `lastChanged` | string |  |
| `links[]` | array<object> |  |
| `links[].href` | string |  |
| `links[].method` | string |  |
| `links[].rel` | string |  |
| `links[].targetSchema` | string |  |
| `listId` | string |  |
| `location` | object |  |
| `location.countryCode` | string |  |
| `location.dstoff` | number |  |
| `location.gmtoff` | number |  |
| `location.latitude` | number |  |
| `location.longitude` | number |  |
| `location.region` | string |  |
| `location.timezone` | string |  |
| `memberRating` | number |  |
| `mergeFields` | object |  |
| `mergeFields.aDDRESS` | object |  |
| `mergeFields.aDDRESS.addr1` | string |  |
| `mergeFields.aDDRESS.addr2` | string |  |
| `mergeFields.aDDRESS.city` | string |  |
| `mergeFields.aDDRESS.country` | string |  |
| `mergeFields.aDDRESS.state` | string |  |
| `mergeFields.aDDRESS.zip` | string |  |
| `mergeFields.bIRTHDAY` | string |  |
| `mergeFields.cOMPANY` | string |  |
| `mergeFields.fNAME` | string |  |
| `mergeFields.lNAME` | string |  |
| `mergeFields.pHONE` | string |  |
| `smsPhoneNumber` | string |  |
| `smsSubscriptionLastUpdated` | string |  |
| `smsSubscriptionStatus` | string |  |
| `source` | string |  |
| `stats` | object |  |
| `stats.avgClickRate` | number |  |
| `stats.avgOpenRate` | number |  |
| `status` | string |  |
| `tags[]` | array<string> |  |
| `tagsCount` | number |  |
| `timestampOpt` | string |  |
| `timestampSignup` | string |  |
| `uniqueEmailId` | string |  |
| `vip` | boolean |  |
| `webId` | number |  |

## Native endpoint

Through the native Mailchimp API, this operation is `GET lists/:list_id/members/:subscriber_hash` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-audience-member.md) for the provider-specific parameters and requirements.

