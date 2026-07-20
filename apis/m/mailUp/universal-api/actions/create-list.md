# MailUp: Create List

Creates a new list in MailUp.

```
POST https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/create-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/create-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/create-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | no |  |
| `city` | string | no |  |
| `companyName` | string | no |  |
| `contactName` | string | no |  |
| `countryCode` | string | no |  |
| `name` | string | yes |  |
| `nlSenderName` | string | no |  |
| `permissionReminder` | string | no |  |
| `webSiteUrl` | string | no |  |
| `ownerEmail` | string | no |  |
| `replyTo` | string | no |  |
| `displayAs` | string | no |  |
| `description` | string | no |  |
| `business` | boolean | no |  |
| `customer` | boolean | no |  |
| `useDefaultSettings` | boolean | no |  |
| `idSettings` | number | no |  |
| `copyFromWebhooks` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "bouncedEmail": "ava@example.com",
      "business": true,
      "charset": "string",
      "city": "string",
      "companyName": "Ava Chen",
      "contactName": "Ava Chen",
      "conversionlabTrackCode": "string",
      "countryCode": "string",
      "customer": true,
      "defaultPrefix": "string",
      "description": "string",
      "disclaimer": "string",
      "displayAs": "string",
      "format": "string",
      "frontendForm": true,
      "headerListUnsubscriber": "string",
      "headerXAbuse": "string",
      "idList": 1,
      "kBMax": 1,
      "linkTrackingParameters": "https://example.com",
      "listGuid": "string",
      "multiOptoutList": "string",
      "multipartText": true,
      "name": "Ava Chen",
      "nLSenderName": "Ava Chen",
      "notifyEmail": "ava@example.com",
      "optoutType": 1,
      "ownerEmail": "ava@example.com",
      "permissionReminder": "string",
      "phone": "string",
      "postalCode": "string",
      "public": true,
      "replyTo": "string",
      "scopeCode": 1,
      "sendConfirmSms": true,
      "sendEmailOptout": true,
      "smsSenderName": "Ava Chen",
      "stateOrProvince": "string",
      "subscribedEmail": true,
      "timeZoneCode": "string",
      "trackOnOpened": true,
      "webSiteUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `bouncedEmail` | string |  |
| `business` | boolean |  |
| `charset` | string |  |
| `city` | string |  |
| `companyName` | string |  |
| `contactName` | string |  |
| `conversionlabTrackCode` | string |  |
| `countryCode` | string |  |
| `customer` | boolean |  |
| `defaultPrefix` | string |  |
| `description` | string |  |
| `disclaimer` | string |  |
| `displayAs` | string |  |
| `format` | string |  |
| `frontendForm` | boolean |  |
| `headerListUnsubscriber` | string |  |
| `headerXAbuse` | string |  |
| `idList` | number |  |
| `kBMax` | number |  |
| `linkTrackingParameters` | string |  |
| `listGuid` | string |  |
| `multiOptoutList` | string |  |
| `multipartText` | boolean |  |
| `name` | string |  |
| `nLSenderName` | string |  |
| `notifyEmail` | string |  |
| `optoutType` | number |  |
| `ownerEmail` | string |  |
| `permissionReminder` | string |  |
| `phone` | string |  |
| `postalCode` | string |  |
| `public` | boolean |  |
| `replyTo` | string |  |
| `scopeCode` | number |  |
| `sendConfirmSms` | boolean |  |
| `sendEmailOptout` | boolean |  |
| `smsSenderName` | string |  |
| `stateOrProvince` | string |  |
| `subscribedEmail` | boolean |  |
| `timeZoneCode` | string |  |
| `trackOnOpened` | boolean |  |
| `webSiteUrl` | string |  |

## Native endpoint

Through the native MailUp API, this operation is `POST Console/List` (base URL `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list.md) for the provider-specific parameters and requirements.

