# RingCentral Universal API Examples

These examples use the MindCloud API key and RingCentral connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info

Retrieves the current RingCentral account information.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/get-account-info?${params}`, {
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
      "bsid": "string",
      "federated": true,
      "id": "string",
      "limits": {
        "cloudRecordingStorage": 1,
        "freeSoftPhoneLinesPerExtension": 1,
        "maxExtensionNumberLength": 1,
        "maxMonitoredExtensionsPerUser": 1,
        "meetingSize": 1
      },
      "mainNumber": "string",
      "operator": {
        "extensionNumber": "string",
        "id": "string",
        "uri": "string"
      },
      "regionalSettings": {
        "currency": {
          "code": "string",
          "id": "string",
          "minorSymbol": "string",
          "name": "Ava Chen",
          "symbol": "string"
        },
        "formattingLocale": {
          "id": "string",
          "localeCode": "string",
          "name": "Ava Chen"
        },
        "greetingLanguage": {
          "id": "string",
          "localeCode": "string",
          "name": "Ava Chen"
        },
        "homeCountry": {
          "id": "string",
          "name": "Ava Chen",
          "uri": "string"
        },
        "language": {
          "id": "string",
          "localeCode": "string",
          "name": "Ava Chen"
        },
        "timeFormat": "string",
        "timezone": {
          "bias": "string",
          "description": "string",
          "id": "string",
          "name": "Ava Chen",
          "uri": "string"
        }
      },
      "serviceInfo": {
        "billingPlan": {
          "duration": 1,
          "durationUnit": "string",
          "id": "string",
          "includedPhoneLines": 1,
          "name": "Ava Chen",
          "type": "string"
        },
        "brand": {
          "homeCountry": {
            "callingCode": "string",
            "id": "string",
            "isoCode": "string",
            "name": "Ava Chen",
            "uri": "string"
          },
          "id": "string",
          "name": "Ava Chen"
        },
        "contractedCountry": {
          "id": "string",
          "isoCode": "string",
          "name": "Ava Chen",
          "uri": "string"
        },
        "servicePlan": {
          "edition": "string",
          "id": "string",
          "name": "Ava Chen"
        },
        "uri": "string"
      },
      "setupWizardState": "string",
      "signupInfo": {
        "creationTime": "string",
        "marketingAccepted": true,
        "tosAccepted": true
      },
      "status": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ringCentral/latest/actions/get-account-info).

## Send SMS

Sends an SMS message from a RingCentral extension.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/send-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "extensionId": "string",
  "from.phoneNumber": "string",
  "to.phoneNumber[]": [
    "string"
  ],
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/send-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "extensionId": "string",
    "from.phoneNumber": "string",
    "to.phoneNumber[]": ["string"],
    "text": "string"
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
      "availability": "string",
      "creationTime": "string",
      "direction": "string",
      "from": {},
      "id": "string",
      "subject": "string",
      "to": [
        {}
      ],
      "type": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

See the full [Send SMS action reference](actions/send-sms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ringCentral/latest/actions/send-sms).
