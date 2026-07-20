# MailUp: Get List

Retrieves a list from MailUp by list ID.

```
GET https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/get-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/get-list?connectionId=$CONNECTION_ID&idList=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idList": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/get-list?${params}`, {
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
| `idList` | number | yes |  |

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

Through the native MailUp API, this operation is `GET Console/List/:id_List` (base URL `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list.md) for the provider-specific parameters and requirements.

