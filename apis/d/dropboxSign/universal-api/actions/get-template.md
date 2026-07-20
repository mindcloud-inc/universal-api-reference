# Dropbox Sign: Get Template

Retrieves a template from Dropbox Sign by ID.

```
GET https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-template?connectionId=$CONNECTION_ID&template_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "template_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-template?${params}`, {
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
| `template_id` | string | yes | The id of the Template to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accounts": [
        {
          "accountId": "string",
          "emailAddress": "ava@example.com",
          "isLocked": true,
          "isPaidHf": true,
          "isPaidHs": true,
          "quotas": {
            "apiSignatureRequestsLeft": 1,
            "documentsLeft": 1,
            "templatesLeft": 1,
            "templatesTotal": 1
          },
          "settings": {
            "signerAccessCodes": true,
            "smsAuthentication": true,
            "smsDelivery": true
          }
        }
      ],
      "canEdit": true,
      "documents": [
        {
          "formFields": [
            {
              "apiId": "string",
              "fontSize": 1,
              "group": {},
              "height": 1,
              "name": "Ava Chen",
              "required": true,
              "signer": 1,
              "type": "string",
              "width": 1,
              "x": 1,
              "y": 1
            }
          ],
          "index": 1,
          "name": "Ava Chen"
        }
      ],
      "isCreator": true,
      "isEmbedded": true,
      "isLocked": true,
      "message": "string",
      "namedFormFields": [
        {
          "apiId": "Ava Chen",
          "fontSize": 1,
          "group": {},
          "height": 1,
          "name": "Ava Chen",
          "required": true,
          "signer": 1,
          "type": "Ava Chen",
          "width": 1,
          "x": 1,
          "y": 1
        }
      ],
      "reusableFormId": "string",
      "signerExperience": {
        "formView": "string"
      },
      "signerRoles": [
        {
          "name": "Ava Chen",
          "order": 1
        }
      ],
      "templateId": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts[].accountId` | string |  |
| `accounts[].emailAddress` | string |  |
| `accounts[].isLocked` | boolean |  |
| `accounts[].isPaidHf` | boolean |  |
| `accounts[].isPaidHs` | boolean |  |
| `accounts[].quotas.apiSignatureRequestsLeft` | number |  |
| `accounts[].quotas.documentsLeft` | number |  |
| `accounts[].quotas.templatesLeft` | number |  |
| `accounts[].quotas.templatesTotal` | number |  |
| `accounts[].settings.signerAccessCodes` | boolean |  |
| `accounts[].settings.smsAuthentication` | boolean |  |
| `accounts[].settings.smsDelivery` | boolean |  |
| `canEdit` | boolean |  |
| `documents[].formFields[].apiId` | string |  |
| `documents[].formFields[].fontSize` | number |  |
| `documents[].formFields[].group` | object |  |
| `documents[].formFields[].height` | number |  |
| `documents[].formFields[].name` | string |  |
| `documents[].formFields[].required` | boolean |  |
| `documents[].formFields[].signer` | number |  |
| `documents[].formFields[].type` | string |  |
| `documents[].formFields[].width` | number |  |
| `documents[].formFields[].x` | number |  |
| `documents[].formFields[].y` | number |  |
| `documents[].index` | number |  |
| `documents[].name` | string |  |
| `isCreator` | boolean |  |
| `isEmbedded` | boolean |  |
| `isLocked` | boolean |  |
| `message` | string |  |
| `namedFormFields[].apiId` | string |  |
| `namedFormFields[].fontSize` | number |  |
| `namedFormFields[].group` | object |  |
| `namedFormFields[].height` | number |  |
| `namedFormFields[].name` | string |  |
| `namedFormFields[].required` | boolean |  |
| `namedFormFields[].signer` | number |  |
| `namedFormFields[].type` | string |  |
| `namedFormFields[].width` | number |  |
| `namedFormFields[].x` | number |  |
| `namedFormFields[].y` | number |  |
| `reusableFormId` | string |  |
| `signerExperience.formView` | string |  |
| `signerRoles[].name` | string |  |
| `signerRoles[].order` | number |  |
| `templateId` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Dropbox Sign API, this operation is `GET /template/:template_id` (base URL `https://api.hellosign.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

