# Global Patron: Create Submission

Creates a form submission in Global Patron.

```
POST https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/create-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Patron `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/create-submission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "formFields[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/create-submission', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "formFields[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | ID of the form receiving the submission. |
| `formFields[]` | array<object> | yes | Submission field values array from the GlobalPatron form definition. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionSuccessful": true,
      "cloudDatabasePostExpectedButFailed": true,
      "emailAddressPostExpectedButFailed": true,
      "id": "string",
      "message": "string",
      "thanksBehaviour": "string",
      "thanksBehaviourMessage": "string",
      "thanksBehaviourRedirectParentPage": true,
      "thanksBehaviourRedirectUrl": "https://example.com",
      "thanksBehaviourRedirectUrlParams": [
        {
          "paramName": "https://example.com",
          "paramValueFixed": "https://example.com",
          "paramValueFormFieldSystemName": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionSuccessful` | boolean | Whether GlobalPatron reports the submission was successful. |
| `cloudDatabasePostExpectedButFailed` | boolean | Whether a cloud database post was expected and failed. |
| `emailAddressPostExpectedButFailed` | boolean | Whether an email post was expected and failed. |
| `id` | string | Created submission identifier. |
| `message` | string | Provider status message. |
| `thanksBehaviour` | string | Configured thanks-page behavior. |
| `thanksBehaviourMessage` | string | Inline thanks message when returned. |
| `thanksBehaviourRedirectParentPage` | boolean | Whether redirects should target the parent page. |
| `thanksBehaviourRedirectUrl` | string | Redirect URL when returned. |
| `thanksBehaviourRedirectUrlParams` | array<object> | Redirect URL parameters when returned. |
| `thanksBehaviourRedirectUrlParams[].paramName` | string | Redirect parameter name. |
| `thanksBehaviourRedirectUrlParams[].paramValueFixed` | string | Fixed redirect parameter value. |
| `thanksBehaviourRedirectUrlParams[].paramValueFormFieldSystemName` | string | Form field used for the redirect parameter. |

## Native endpoint

Through the native Global Patron API, this operation is `POST /api/form/{formId}/submission` (base URL `https://api.globalpatron.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-submission.md) for the provider-specific parameters and requirements.

