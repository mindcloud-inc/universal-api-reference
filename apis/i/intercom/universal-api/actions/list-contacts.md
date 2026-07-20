# Intercom: List Contacts



```
GET https://connect.mindcloud.co/v1/universal/intercom/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intercom `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intercom/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intercom/latest/actions/list-contacts?${params}`, {
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
      "androidAppName": {},
      "androidAppVersion": {},
      "androidDevice": {},
      "androidLastSeenAt": {},
      "androidOsVersion": {},
      "androidSdkVersion": {},
      "avatar": {},
      "browser": {},
      "browserLanguage": {},
      "browserVersion": {},
      "companies": {
        "data": [
          {
            "id": "string",
            "type": "string",
            "url": "https://example.com"
          }
        ],
        "hasMore": true,
        "totalCount": 1,
        "type": "string",
        "url": "https://example.com"
      },
      "createdAt": 1,
      "email": "ava@example.com",
      "enabledPushMessaging": {},
      "externalId": "string",
      "hasHardBounced": true,
      "id": "string",
      "iosAppName": {},
      "iosAppVersion": {},
      "iosDevice": {},
      "iosLastSeenAt": {},
      "iosOsVersion": {},
      "iosSdkVersion": {},
      "languageOverride": {},
      "lastContactedAt": {},
      "lastEmailClickedAt": {},
      "lastEmailOpenedAt": {},
      "lastRepliedAt": 1,
      "lastSeenAt": 1,
      "location": {
        "city": {},
        "continentCode": {},
        "country": {},
        "countryCode": {},
        "region": {},
        "type": "string"
      },
      "markedEmailAsSpam": true,
      "name": "Ava Chen",
      "notes": {
        "hasMore": true,
        "totalCount": 1,
        "type": "string",
        "url": "https://example.com"
      },
      "optedInSubscriptionTypes": {
        "hasMore": true,
        "totalCount": 1,
        "type": "string",
        "url": "https://example.com"
      },
      "optedOutSubscriptionTypes": {
        "hasMore": true,
        "totalCount": 1,
        "type": "string",
        "url": "https://example.com"
      },
      "os": {},
      "ownerId": {},
      "phone": {},
      "referrer": {},
      "role": "string",
      "signedUpAt": 1,
      "smsConsent": true,
      "socialProfiles": {
        "type": "string"
      },
      "tags": {
        "hasMore": true,
        "totalCount": 1,
        "type": "string",
        "url": "https://example.com"
      },
      "type": "string",
      "unsubscribedFromEmails": true,
      "unsubscribedFromSms": true,
      "updatedAt": 1,
      "utmCampaign": {},
      "utmContent": {},
      "utmMedium": {},
      "utmSource": {},
      "utmTerm": {},
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `androidAppName` | object |  |
| `androidAppVersion` | object |  |
| `androidDevice` | object |  |
| `androidLastSeenAt` | object |  |
| `androidOsVersion` | object |  |
| `androidSdkVersion` | object |  |
| `avatar` | object |  |
| `browser` | object |  |
| `browserLanguage` | object |  |
| `browserVersion` | object |  |
| `companies.data[].id` | string |  |
| `companies.data[].type` | string |  |
| `companies.data[].url` | string |  |
| `companies.hasMore` | boolean |  |
| `companies.totalCount` | number |  |
| `companies.type` | string |  |
| `companies.url` | string |  |
| `createdAt` | number |  |
| `email` | string |  |
| `enabledPushMessaging` | object |  |
| `externalId` | string |  |
| `hasHardBounced` | boolean |  |
| `id` | string |  |
| `iosAppName` | object |  |
| `iosAppVersion` | object |  |
| `iosDevice` | object |  |
| `iosLastSeenAt` | object |  |
| `iosOsVersion` | object |  |
| `iosSdkVersion` | object |  |
| `languageOverride` | object |  |
| `lastContactedAt` | object |  |
| `lastEmailClickedAt` | object |  |
| `lastEmailOpenedAt` | object |  |
| `lastRepliedAt` | number |  |
| `lastSeenAt` | number |  |
| `location.city` | object |  |
| `location.continentCode` | object |  |
| `location.country` | object |  |
| `location.countryCode` | object |  |
| `location.region` | object |  |
| `location.type` | string |  |
| `markedEmailAsSpam` | boolean |  |
| `name` | string |  |
| `notes.hasMore` | boolean |  |
| `notes.totalCount` | number |  |
| `notes.type` | string |  |
| `notes.url` | string |  |
| `optedInSubscriptionTypes.hasMore` | boolean |  |
| `optedInSubscriptionTypes.totalCount` | number |  |
| `optedInSubscriptionTypes.type` | string |  |
| `optedInSubscriptionTypes.url` | string |  |
| `optedOutSubscriptionTypes.hasMore` | boolean |  |
| `optedOutSubscriptionTypes.totalCount` | number |  |
| `optedOutSubscriptionTypes.type` | string |  |
| `optedOutSubscriptionTypes.url` | string |  |
| `os` | object |  |
| `ownerId` | object |  |
| `phone` | object |  |
| `referrer` | object |  |
| `role` | string |  |
| `signedUpAt` | number |  |
| `smsConsent` | boolean |  |
| `socialProfiles.type` | string |  |
| `tags.hasMore` | boolean |  |
| `tags.totalCount` | number |  |
| `tags.type` | string |  |
| `tags.url` | string |  |
| `type` | string |  |
| `unsubscribedFromEmails` | boolean |  |
| `unsubscribedFromSms` | boolean |  |
| `updatedAt` | number |  |
| `utmCampaign` | object |  |
| `utmContent` | object |  |
| `utmMedium` | object |  |
| `utmSource` | object |  |
| `utmTerm` | object |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Intercom API, this operation is `GET /contacts` (base URL `https://api.intercom.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

