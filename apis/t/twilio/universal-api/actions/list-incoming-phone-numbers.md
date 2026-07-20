# Twilio: List Incoming Phone Numbers

Retrieves incoming phone numbers from Twilio.

```
GET https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-incoming-phone-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twilio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-incoming-phone-numbers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-incoming-phone-numbers?${params}`, {
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
| `phoneNumber` | string | no |  |
| `friendlyName` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end": 1,
      "firstPageUri": "string",
      "incomingPhoneNumbers": [
        {
          "accountSid": "string",
          "addressRequirements": "string",
          "addressSid": "string",
          "apiVersion": "string",
          "beta": true,
          "bundleSid": "string",
          "capabilities": {
            "fax": true,
            "mms": true,
            "sms": true,
            "voice": true
          },
          "dateCreated": "string",
          "dateUpdated": "string",
          "emergencyAddressSid": "string",
          "emergencyAddressStatus": "string",
          "emergencyStatus": "string",
          "friendlyName": "Ava Chen",
          "identitySid": "string",
          "origin": "string",
          "phoneNumber": "string",
          "sid": "string",
          "smsApplicationSid": "string",
          "smsFallbackMethod": "string",
          "smsFallbackUrl": "https://example.com",
          "smsMethod": "string",
          "smsUrl": "https://example.com",
          "status": "string",
          "statusCallback": "string",
          "statusCallbackMethod": "string",
          "subresourceUris": {
            "assignedAddOns": "string"
          },
          "trunkSid": "string",
          "type": "string",
          "uri": "string",
          "voiceApplicationSid": "string",
          "voiceCallerIdLookup": true,
          "voiceFallbackMethod": "string",
          "voiceFallbackUrl": "https://example.com",
          "voiceMethod": "string",
          "voiceReceiveMode": "string",
          "voiceUrl": "https://example.com"
        }
      ],
      "nextPageUri": "string",
      "page": 1,
      "pageSize": 1,
      "previousPageUri": "string",
      "start": 1,
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end` | number |  |
| `firstPageUri` | string |  |
| `incomingPhoneNumbers[].accountSid` | string |  |
| `incomingPhoneNumbers[].addressRequirements` | string |  |
| `incomingPhoneNumbers[].addressSid` | string |  |
| `incomingPhoneNumbers[].apiVersion` | string |  |
| `incomingPhoneNumbers[].beta` | boolean |  |
| `incomingPhoneNumbers[].bundleSid` | string |  |
| `incomingPhoneNumbers[].capabilities.fax` | boolean |  |
| `incomingPhoneNumbers[].capabilities.mms` | boolean |  |
| `incomingPhoneNumbers[].capabilities.sms` | boolean |  |
| `incomingPhoneNumbers[].capabilities.voice` | boolean |  |
| `incomingPhoneNumbers[].dateCreated` | string |  |
| `incomingPhoneNumbers[].dateUpdated` | string |  |
| `incomingPhoneNumbers[].emergencyAddressSid` | string |  |
| `incomingPhoneNumbers[].emergencyAddressStatus` | string |  |
| `incomingPhoneNumbers[].emergencyStatus` | string |  |
| `incomingPhoneNumbers[].friendlyName` | string |  |
| `incomingPhoneNumbers[].identitySid` | string |  |
| `incomingPhoneNumbers[].origin` | string |  |
| `incomingPhoneNumbers[].phoneNumber` | string |  |
| `incomingPhoneNumbers[].sid` | string |  |
| `incomingPhoneNumbers[].smsApplicationSid` | string |  |
| `incomingPhoneNumbers[].smsFallbackMethod` | string |  |
| `incomingPhoneNumbers[].smsFallbackUrl` | string |  |
| `incomingPhoneNumbers[].smsMethod` | string |  |
| `incomingPhoneNumbers[].smsUrl` | string |  |
| `incomingPhoneNumbers[].status` | string |  |
| `incomingPhoneNumbers[].statusCallback` | string |  |
| `incomingPhoneNumbers[].statusCallbackMethod` | string |  |
| `incomingPhoneNumbers[].subresourceUris.assignedAddOns` | string |  |
| `incomingPhoneNumbers[].trunkSid` | string |  |
| `incomingPhoneNumbers[].type` | string |  |
| `incomingPhoneNumbers[].uri` | string |  |
| `incomingPhoneNumbers[].voiceApplicationSid` | string |  |
| `incomingPhoneNumbers[].voiceCallerIdLookup` | boolean |  |
| `incomingPhoneNumbers[].voiceFallbackMethod` | string |  |
| `incomingPhoneNumbers[].voiceFallbackUrl` | string |  |
| `incomingPhoneNumbers[].voiceMethod` | string |  |
| `incomingPhoneNumbers[].voiceReceiveMode` | string |  |
| `incomingPhoneNumbers[].voiceUrl` | string |  |
| `nextPageUri` | string |  |
| `page` | number |  |
| `pageSize` | number |  |
| `previousPageUri` | string |  |
| `start` | number |  |
| `uri` | string |  |

## Native endpoint

Through the native Twilio API, this operation is `GET /Accounts/:AccountSid/IncomingPhoneNumbers.json` (base URL `https://api.twilio.com/2010-04-01`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-incoming-phone-numbers.md) for the provider-specific parameters and requirements.

