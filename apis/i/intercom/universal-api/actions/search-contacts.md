# Intercom: Search Contacts



```
GET https://connect.mindcloud.co/v1/universal/intercom/latest/actions/search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intercom `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intercom/latest/actions/search-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0&query.field=string&query.operator=string&query.value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query.field": "string",
  "query.operator": "string",
  "query.value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intercom/latest/actions/search-contacts?${params}`, {
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
| `query` | object | no |  |
| `query.field` | string | yes | Field to search by |
| `query.operator` | string | yes | Search operator |
| `query.value` | string | yes | Value to match |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      "pages": {
        "page": 1,
        "perPage": 1,
        "totalPages": 1,
        "type": "string"
      },
      "totalCount": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].androidAppName` | string |  |
| `data[].androidAppVersion` | string |  |
| `data[].androidDevice` | string |  |
| `data[].androidLastSeenAt` | string |  |
| `data[].androidOsVersion` | string |  |
| `data[].androidSdkVersion` | string |  |
| `data[].avatar` | string |  |
| `data[].browser` | string |  |
| `data[].browserLanguage` | string |  |
| `data[].browserVersion` | string |  |
| `data[].companies` | object |  |
| `data[].companies.data` | array<string> |  |
| `data[].companies.hasMore` | boolean |  |
| `data[].companies.totalCount` | number |  |
| `data[].companies.type` | string |  |
| `data[].companies.url` | string |  |
| `data[].createdAt` | number |  |
| `data[].customAttributes` | object |  |
| `data[].email` | string |  |
| `data[].enabledPushMessaging` | string |  |
| `data[].externalId` | string |  |
| `data[].hasHardBounced` | boolean |  |
| `data[].id` | string |  |
| `data[].iosAppName` | string |  |
| `data[].iosAppVersion` | string |  |
| `data[].iosDevice` | string |  |
| `data[].iosLastSeenAt` | string |  |
| `data[].iosOsVersion` | string |  |
| `data[].iosSdkVersion` | string |  |
| `data[].languageOverride` | string |  |
| `data[].lastContactedAt` | string |  |
| `data[].lastEmailClickedAt` | string |  |
| `data[].lastEmailOpenedAt` | string |  |
| `data[].lastRepliedAt` | string |  |
| `data[].lastSeenAt` | string |  |
| `data[].location` | object |  |
| `data[].location.city` | string |  |
| `data[].location.continentCode` | string |  |
| `data[].location.country` | string |  |
| `data[].location.countryCode` | string |  |
| `data[].location.region` | string |  |
| `data[].location.type` | string |  |
| `data[].markedEmailAsSpam` | boolean |  |
| `data[].name` | string |  |
| `data[].notes` | object |  |
| `data[].notes.data` | array<string> |  |
| `data[].notes.hasMore` | boolean |  |
| `data[].notes.totalCount` | number |  |
| `data[].notes.type` | string |  |
| `data[].notes.url` | string |  |
| `data[].optedInSubscriptionTypes` | object |  |
| `data[].optedInSubscriptionTypes.data` | array<string> |  |
| `data[].optedInSubscriptionTypes.hasMore` | boolean |  |
| `data[].optedInSubscriptionTypes.totalCount` | number |  |
| `data[].optedInSubscriptionTypes.type` | string |  |
| `data[].optedInSubscriptionTypes.url` | string |  |
| `data[].optedOutSubscriptionTypes` | object |  |
| `data[].optedOutSubscriptionTypes.data` | array<string> |  |
| `data[].optedOutSubscriptionTypes.hasMore` | boolean |  |
| `data[].optedOutSubscriptionTypes.totalCount` | number |  |
| `data[].optedOutSubscriptionTypes.type` | string |  |
| `data[].optedOutSubscriptionTypes.url` | string |  |
| `data[].os` | string |  |
| `data[].ownerId` | string |  |
| `data[].phone` | string |  |
| `data[].referrer` | string |  |
| `data[].role` | string |  |
| `data[].signedUpAt` | string |  |
| `data[].smsConsent` | boolean |  |
| `data[].socialProfiles` | object |  |
| `data[].socialProfiles.data` | array<string> |  |
| `data[].socialProfiles.type` | string |  |
| `data[].tags` | object |  |
| `data[].tags.data` | array<string> |  |
| `data[].tags.hasMore` | boolean |  |
| `data[].tags.totalCount` | number |  |
| `data[].tags.type` | string |  |
| `data[].tags.url` | string |  |
| `data[].type` | string |  |
| `data[].unsubscribedFromEmails` | boolean |  |
| `data[].unsubscribedFromSms` | boolean |  |
| `data[].updatedAt` | number |  |
| `data[].utmCampaign` | string |  |
| `data[].utmContent` | string |  |
| `data[].utmMedium` | string |  |
| `data[].utmSource` | string |  |
| `data[].utmTerm` | string |  |
| `data[].workspaceId` | string |  |
| `pages` | object |  |
| `pages.page` | number |  |
| `pages.perPage` | number |  |
| `pages.totalPages` | number |  |
| `pages.type` | string |  |
| `totalCount` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Intercom API, this operation is `POST /contacts/search` (base URL `https://api.intercom.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-contacts.md) for the provider-specific parameters and requirements.

