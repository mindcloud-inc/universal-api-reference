# Kite Suite: Create Form Mailchimp Integration



```
POST https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-form-mailchimp-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-form-mailchimp-integration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "form": "string",
  "listId": "string",
  "tagType": "string",
  "staticTags[]": [
    "string"
  ],
  "dynamicTag": "string",
  "sendContact": "string",
  "consentMessage": "string",
  "isUpdateExistingContact": true,
  "isAddExistingContact": true,
  "isSendOptIn": true,
  "fields[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-form-mailchimp-integration', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "form": "string",
    "listId": "string",
    "tagType": "string",
    "staticTags[]": ["string"],
    "dynamicTag": "string",
    "sendContact": "string",
    "consentMessage": "string",
    "isUpdateExistingContact": true,
    "isAddExistingContact": true,
    "isSendOptIn": true,
    "fields[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `form` | string | yes | ID of the form. |
| `listId` | string | yes | ID of the Mailchimp list. |
| `tagType` | string | yes | Type of Mailchimp tags. |
| `staticTags[]` | array | yes | Array of static Mailchimp tags. |
| `dynamicTag` | string | yes | ID of the form field for dynamic Mailchimp tag. |
| `sendContact` | string | yes | How to send contact to Mailchimp. |
| `consentMessage` | string | yes | Consent message for Mailchimp. |
| `isUpdateExistingContact` | boolean | yes | Flag to update existing contact in Mailchimp. |
| `isAddExistingContact` | boolean | yes | Flag to add existing contact in Mailchimp. |
| `isSendOptIn` | boolean | yes | Flag to send opt-in email to contact. |
| `fields[]` | array | yes | Array of Mailchimp fields and corresponding form fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object | Created form integration object. |

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/form/integration/mailchimp` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form-mailchimp-integration.md) for the provider-specific parameters and requirements.

