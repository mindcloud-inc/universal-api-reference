# Data8: Cleanse Email Address

Cleanses an email address with Data8.

```
GET https://connect.mindcloud.co/v1/universal/data8/latest/actions/cleanse-email-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Data8 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/data8/latest/actions/cleanse-email-address?connectionId=$CONNECTION_ID&email=ava%40example.com&level=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com",
  "level": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/data8/latest/actions/cleanse-email-address?${params}`, {
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
| `email` | string | yes | The email address to validate. |
| `level` | string | yes | The validation level to apply. |
| `record` | object | no | Optional supporting identity data used to enrich email cleansing results. |
| `options` | object | no | Optional settings that control email validation behavior. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "EmailType": "ava@example.com",
      "OriginalValid": true,
      "ParsedName": {
        "Forename": "Ava Chen",
        "Surname": "Ava Chen"
      },
      "Result": "string",
      "Status": {
        "CreditsRemaining": 1,
        "ErrorMessage": "string",
        "Success": true
      },
      "SuggestedEmailAddress": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `EmailType` | string |  |
| `OriginalValid` | boolean |  |
| `ParsedName.Forename` | string |  |
| `ParsedName.Surname` | string |  |
| `Result` | string |  |
| `Status.CreditsRemaining` | number |  |
| `Status.ErrorMessage` | string |  |
| `Status.Success` | boolean |  |
| `SuggestedEmailAddress` | string |  |

## Native endpoint

Through the native Data8 API, this operation is `POST /EmailValidation/Cleanse.json` (base URL `https://webservices.data-8.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cleanse-email-address.md) for the provider-specific parameters and requirements.

