# Easymailing: Get Audience

Retrieves an audience from Easymailing.

```
GET https://connect.mindcloud.co/v1/universal/easymailing/latest/actions/get-audience
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easymailing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easymailing/latest/actions/get-audience?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easymailing/latest/actions/get-audience?${params}`, {
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
| `uuid` | string | yes | Audience UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeSuscribers": 1,
      "audienceResources": {
        "automations": 1,
        "campaigns": 1,
        "landingPages": 1,
        "subscriptionForms": 1
      },
      "audienceStats": {
        "active": 1,
        "canceled": 1,
        "score": {},
        "total": 1
      },
      "company": {
        "address": {},
        "city": {},
        "companyName": "Ava Chen",
        "country": {},
        "logoUrl": {},
        "phone": {},
        "postalCode": {},
        "state": {},
        "websiteUrl": {}
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "description": {},
      "groups": [
        {
          "color": "string",
          "description": "string",
          "public": true,
          "suscriberCount": 1,
          "title": "string"
        }
      ],
      "id": 1,
      "listGdpr": {
        "dataManager": {},
        "enabled": true,
        "privacyUrl": {},
        "uuid": "string"
      },
      "notifications": {
        "optIn": "string",
        "optInNotifyEmail": {},
        "optOut": "string",
        "optOutNotifyEmail": {},
        "unsubscribeHardBounces": true,
        "unsubscribeSoftBounces": true,
        "welcomeEmail": true
      },
      "preferences": {
        "fromEmail": {},
        "fromName": "Ava Chen",
        "replyTo": {}
      },
      "timezone": "string",
      "title": "string",
      "totalSuscribers": 1,
      "unsuscribed": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeSuscribers` | number |  |
| `audienceResources.automations` | number |  |
| `audienceResources.campaigns` | number |  |
| `audienceResources.landingPages` | number |  |
| `audienceResources.subscriptionForms` | number |  |
| `audienceStats.active` | number |  |
| `audienceStats.canceled` | number |  |
| `audienceStats.score` | object |  |
| `audienceStats.total` | number |  |
| `company.address` | object |  |
| `company.city` | object |  |
| `company.companyName` | string |  |
| `company.country` | object |  |
| `company.logoUrl` | object |  |
| `company.phone` | object |  |
| `company.postalCode` | object |  |
| `company.state` | object |  |
| `company.websiteUrl` | object |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `description` | object |  |
| `groups[].color` | string |  |
| `groups[].description` | string |  |
| `groups[].public` | boolean |  |
| `groups[].suscriberCount` | number |  |
| `groups[].title` | string |  |
| `id` | number |  |
| `listGdpr.dataManager` | object |  |
| `listGdpr.enabled` | boolean |  |
| `listGdpr.privacyUrl` | object |  |
| `listGdpr.uuid` | string |  |
| `notifications.optIn` | string |  |
| `notifications.optInNotifyEmail` | object |  |
| `notifications.optOut` | string |  |
| `notifications.optOutNotifyEmail` | object |  |
| `notifications.unsubscribeHardBounces` | boolean |  |
| `notifications.unsubscribeSoftBounces` | boolean |  |
| `notifications.welcomeEmail` | boolean |  |
| `preferences.fromEmail` | object |  |
| `preferences.fromName` | string |  |
| `preferences.replyTo` | object |  |
| `timezone` | string |  |
| `title` | string |  |
| `totalSuscribers` | number |  |
| `unsuscribed` | number |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Easymailing API, this operation is `GET /audiences/{{uuid}}` (base URL `https://api.easymailing.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-audience.md) for the provider-specific parameters and requirements.

