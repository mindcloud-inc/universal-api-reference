# Intercom Universal API Examples

These examples use the MindCloud API key and Intercom connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Contact



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

Example response:

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

See the full [Get Contact action reference](actions/get-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/intercom/latest/actions/get-contact).

## Archive Contact



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/intercom/latest/actions/archive-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intercom/latest/actions/archive-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "externalId": "string",
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Archive Contact action reference](actions/archive-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/intercom/latest/actions/archive-contact).
