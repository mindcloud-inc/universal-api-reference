# RingCentral: Get Extension

Retrieves an extension from a RingCentral account.

```
GET https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/get-extension
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RingCentral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/get-extension?connectionId=$CONNECTION_ID&accountId=string&extensionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "extensionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/get-extension?${params}`, {
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
| `accountId` | string | yes |  |
| `extensionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedCountry": {
        "id": "string",
        "isoCode": "string",
        "name": "Ava Chen",
        "uri": "string"
      },
      "contact": {
        "email": "ava@example.com",
        "emailAsLoginName": true,
        "firstName": "Ava",
        "lastName": "Chen",
        "pronouncedName": {
          "prompt": {
            "contentType": "Ava Chen",
            "contentUri": "Ava Chen",
            "id": "Ava Chen"
          },
          "text": "Ava Chen",
          "type": "Ava Chen"
        }
      },
      "creationTime": "string",
      "extensionNumber": "string",
      "hidden": true,
      "id": "string",
      "name": "Ava Chen",
      "permissions": {
        "admin": {
          "enabled": true
        },
        "internationalCalling": {
          "enabled": true
        }
      },
      "profileImage": {
        "uri": "string"
      },
      "regionalSettings": {
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
          "callingCode": "string",
          "id": "string",
          "isoCode": "string",
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
      "roles": [
        {
          "autoAssigned": true,
          "displayName": "Ava Chen",
          "id": "string",
          "siteCompatible": true,
          "siteRestricted": true,
          "uri": "string"
        }
      ],
      "setupWizardState": "string",
      "status": "string",
      "type": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedCountry.id` | string |  |
| `assignedCountry.isoCode` | string |  |
| `assignedCountry.name` | string |  |
| `assignedCountry.uri` | string |  |
| `contact.email` | string |  |
| `contact.emailAsLoginName` | boolean |  |
| `contact.firstName` | string |  |
| `contact.lastName` | string |  |
| `contact.pronouncedName.prompt.contentType` | string |  |
| `contact.pronouncedName.prompt.contentUri` | string |  |
| `contact.pronouncedName.prompt.id` | string |  |
| `contact.pronouncedName.text` | string |  |
| `contact.pronouncedName.type` | string |  |
| `creationTime` | string |  |
| `extensionNumber` | string |  |
| `hidden` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `permissions.admin.enabled` | boolean |  |
| `permissions.internationalCalling.enabled` | boolean |  |
| `profileImage.uri` | string |  |
| `regionalSettings.formattingLocale.id` | string |  |
| `regionalSettings.formattingLocale.localeCode` | string |  |
| `regionalSettings.formattingLocale.name` | string |  |
| `regionalSettings.greetingLanguage.id` | string |  |
| `regionalSettings.greetingLanguage.localeCode` | string |  |
| `regionalSettings.greetingLanguage.name` | string |  |
| `regionalSettings.homeCountry.callingCode` | string |  |
| `regionalSettings.homeCountry.id` | string |  |
| `regionalSettings.homeCountry.isoCode` | string |  |
| `regionalSettings.homeCountry.name` | string |  |
| `regionalSettings.homeCountry.uri` | string |  |
| `regionalSettings.language.id` | string |  |
| `regionalSettings.language.localeCode` | string |  |
| `regionalSettings.language.name` | string |  |
| `regionalSettings.timeFormat` | string |  |
| `regionalSettings.timezone.bias` | string |  |
| `regionalSettings.timezone.description` | string |  |
| `regionalSettings.timezone.id` | string |  |
| `regionalSettings.timezone.name` | string |  |
| `regionalSettings.timezone.uri` | string |  |
| `roles[].autoAssigned` | boolean |  |
| `roles[].displayName` | string |  |
| `roles[].id` | string |  |
| `roles[].siteCompatible` | boolean |  |
| `roles[].siteRestricted` | boolean |  |
| `roles[].uri` | string |  |
| `setupWizardState` | string |  |
| `status` | string |  |
| `type` | string |  |
| `uri` | string |  |

## Native endpoint

Through the native RingCentral API, this operation is `GET restapi/v1.0/account/:accountId/extension/:extensionId` (base URL `https://platform.ringcentral.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-extension.md) for the provider-specific parameters and requirements.

