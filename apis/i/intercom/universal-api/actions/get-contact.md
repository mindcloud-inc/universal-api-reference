# Intercom: Get Contact



```
GET https://connect.mindcloud.co/v1/universal/intercom/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intercom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intercom/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intercom/latest/actions/get-contact?${params}`, {
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
| `contactId` | string | yes | Intercom contact identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "androidAppName": "Ava Chen",
      "androidAppVersion": "string",
      "androidDevice": "string",
      "androidLastSeenAt": "string",
      "androidOsVersion": "string",
      "androidSdkVersion": "string",
      "avatar": "string",
      "browser": "string",
      "browserLanguage": "string",
      "browserVersion": "string",
      "companies": {
        "data": [
          "string"
        ],
        "hasMore": true,
        "totalCount": 1,
        "type": "string",
        "url": "https://example.com"
      },
      "createdAt": 1,
      "customAttributes": {},
      "email": "ava@example.com",
      "enabledPushMessaging": "string",
      "externalId": "string",
      "hasHardBounced": true,
      "id": "string",
      "iosAppName": "Ava Chen",
      "iosAppVersion": "string",
      "iosDevice": "string",
      "iosLastSeenAt": "string",
      "iosOsVersion": "string",
      "iosSdkVersion": "string",
      "languageOverride": "string",
      "lastContactedAt": "string",
      "lastEmailClickedAt": "ava@example.com",
      "lastEmailOpenedAt": "ava@example.com",
      "lastRepliedAt": "string",
      "lastSeenAt": "string",
      "location": {
        "city": "string",
        "continentCode": "string",
        "country": "string",
        "countryCode": "string",
        "region": "string",
        "type": "string"
      },
      "markedEmailAsSpam": true,
      "name": "Ava Chen",
      "notes": {
        "data": [
          "string"
        ],
        "hasMore": true,
        "totalCount": 1,
        "type": "string",
        "url": "https://example.com"
      },
      "optedInSubscriptionTypes": {
        "data": [
          "string"
        ],
        "hasMore": true,
        "totalCount": 1,
        "type": "string",
        "url": "https://example.com"
      },
      "optedOutSubscriptionTypes": {
        "data": [
          "string"
        ],
        "hasMore": true,
        "totalCount": 1,
        "type": "string",
        "url": "https://example.com"
      },
      "os": "string",
      "ownerId": "string",
      "phone": "string",
      "referrer": "string",
      "role": "string",
      "signedUpAt": "string",
      "smsConsent": true,
      "socialProfiles": {
        "data": [
          "string"
        ],
        "type": "string"
      },
      "tags": {
        "data": [
          "string"
        ],
        "hasMore": true,
        "totalCount": 1,
        "type": "string",
        "url": "https://example.com"
      },
      "type": "string",
      "unsubscribedFromEmails": true,
      "unsubscribedFromSms": true,
      "updatedAt": 1,
      "utmCampaign": "string",
      "utmContent": "string",
      "utmMedium": "string",
      "utmSource": "string",
      "utmTerm": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `androidAppName` | string |  |
| `androidAppVersion` | string |  |
| `androidDevice` | string |  |
| `androidLastSeenAt` | string |  |
| `androidOsVersion` | string |  |
| `androidSdkVersion` | string |  |
| `avatar` | string |  |
| `browser` | string |  |
| `browserLanguage` | string |  |
| `browserVersion` | string |  |
| `companies` | object |  |
| `companies.data` | array<string> |  |
| `companies.hasMore` | boolean |  |
| `companies.totalCount` | number |  |
| `companies.type` | string |  |
| `companies.url` | string |  |
| `createdAt` | number |  |
| `customAttributes` | object |  |
| `email` | string |  |
| `enabledPushMessaging` | string |  |
| `externalId` | string |  |
| `hasHardBounced` | boolean |  |
| `id` | string |  |
| `iosAppName` | string |  |
| `iosAppVersion` | string |  |
| `iosDevice` | string |  |
| `iosLastSeenAt` | string |  |
| `iosOsVersion` | string |  |
| `iosSdkVersion` | string |  |
| `languageOverride` | string |  |
| `lastContactedAt` | string |  |
| `lastEmailClickedAt` | string |  |
| `lastEmailOpenedAt` | string |  |
| `lastRepliedAt` | string |  |
| `lastSeenAt` | string |  |
| `location` | object |  |
| `location.city` | string |  |
| `location.continentCode` | string |  |
| `location.country` | string |  |
| `location.countryCode` | string |  |
| `location.region` | string |  |
| `location.type` | string |  |
| `markedEmailAsSpam` | boolean |  |
| `name` | string |  |
| `notes` | object |  |
| `notes.data` | array<string> |  |
| `notes.hasMore` | boolean |  |
| `notes.totalCount` | number |  |
| `notes.type` | string |  |
| `notes.url` | string |  |
| `optedInSubscriptionTypes` | object |  |
| `optedInSubscriptionTypes.data` | array<string> |  |
| `optedInSubscriptionTypes.hasMore` | boolean |  |
| `optedInSubscriptionTypes.totalCount` | number |  |
| `optedInSubscriptionTypes.type` | string |  |
| `optedInSubscriptionTypes.url` | string |  |
| `optedOutSubscriptionTypes` | object |  |
| `optedOutSubscriptionTypes.data` | array<string> |  |
| `optedOutSubscriptionTypes.hasMore` | boolean |  |
| `optedOutSubscriptionTypes.totalCount` | number |  |
| `optedOutSubscriptionTypes.type` | string |  |
| `optedOutSubscriptionTypes.url` | string |  |
| `os` | string |  |
| `ownerId` | string |  |
| `phone` | string |  |
| `referrer` | string |  |
| `role` | string |  |
| `signedUpAt` | string |  |
| `smsConsent` | boolean |  |
| `socialProfiles` | object |  |
| `socialProfiles.data` | array<string> |  |
| `socialProfiles.type` | string |  |
| `tags` | object |  |
| `tags.data` | array<string> |  |
| `tags.hasMore` | boolean |  |
| `tags.totalCount` | number |  |
| `tags.type` | string |  |
| `tags.url` | string |  |
| `type` | string |  |
| `unsubscribedFromEmails` | boolean |  |
| `unsubscribedFromSms` | boolean |  |
| `updatedAt` | number |  |
| `utmCampaign` | string |  |
| `utmContent` | string |  |
| `utmMedium` | string |  |
| `utmSource` | string |  |
| `utmTerm` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Intercom API, this operation is `GET /contacts/:contact_id` (base URL `https://api.intercom.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

