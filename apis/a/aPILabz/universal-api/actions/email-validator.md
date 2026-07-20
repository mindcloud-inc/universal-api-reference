# API Labz: Email Validator

Validates an email address with API Labz.

```
GET https://connect.mindcloud.co/v1/universal/aPILabz/latest/actions/email-validator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a API Labz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aPILabz/latest/actions/email-validator?connectionId=$CONNECTION_ID&emailAddress=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emailAddress": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aPILabz/latest/actions/email-validator?${params}`, {
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
| `emailAddress` | string | yes | Email address to validate |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autocorrect": "string",
      "deliverability": "string",
      "email": "ava@example.com",
      "isCatchallEmail": {
        "text": "ava@example.com",
        "value": true
      },
      "isDisposableEmail": {
        "text": "ava@example.com",
        "value": true
      },
      "isFreeEmail": {
        "text": "ava@example.com",
        "value": true
      },
      "isMxFound": {
        "text": "string",
        "value": true
      },
      "isRoleEmail": {
        "text": "ava@example.com",
        "value": true
      },
      "isSmtpValid": {
        "text": "string",
        "value": true
      },
      "isValidFormat": {
        "text": "string",
        "value": true
      },
      "qualityScore": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autocorrect` | string |  |
| `deliverability` | string |  |
| `email` | string |  |
| `isCatchallEmail.text` | string |  |
| `isCatchallEmail.value` | boolean |  |
| `isDisposableEmail.text` | string |  |
| `isDisposableEmail.value` | boolean |  |
| `isFreeEmail.text` | string |  |
| `isFreeEmail.value` | boolean |  |
| `isMxFound.text` | string |  |
| `isMxFound.value` | boolean |  |
| `isRoleEmail.text` | string |  |
| `isRoleEmail.value` | boolean |  |
| `isSmtpValid.text` | string |  |
| `isSmtpValid.value` | boolean |  |
| `isValidFormat.text` | string |  |
| `isValidFormat.value` | boolean |  |
| `qualityScore` | string |  |

## Native endpoint

Through the native API Labz API, this operation is `POST /module/111` (base URL `https://hub.apilabz.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/email-validator.md) for the provider-specific parameters and requirements.

