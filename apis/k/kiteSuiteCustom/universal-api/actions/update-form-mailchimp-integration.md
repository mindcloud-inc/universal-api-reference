# Kite Suite: Update Form Mailchimp Integration



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-mailchimp-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-mailchimp-integration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "id": "string",
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-mailchimp-integration', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "id": "string",
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
| `id` | string | yes | ID of the Mailchimp integration to update. |
| `listId` | string | yes | Updated ID of the Mailchimp list. |
| `tagType` | string | yes | Updated type of Mailchimp tags. |
| `staticTags[]` | array | yes | Updated array of static Mailchimp tags. |
| `dynamicTag` | string | yes | Updated ID of the form field for dynamic Mailchimp tag. |
| `sendContact` | string | yes | Updated how to send contact to Mailchimp. |
| `consentMessage` | string | yes | Updated consent message for Mailchimp. |
| `isUpdateExistingContact` | boolean | yes | Updated flag to update existing contact in Mailchimp. |
| `isAddExistingContact` | boolean | yes | Updated flag to add existing contact in Mailchimp. |
| `isSendOptIn` | boolean | yes | Updated flag to send opt-in email to contact. |
| `fields[]` | array | yes | Updated array of Mailchimp fields and corresponding form fields. |

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
| `value` | object | Updated form integration object. |

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/form/integration/mailchimp/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form-mailchimp-integration.md) for the provider-specific parameters and requirements.

