# Olvy: Validate Email

Validates an email address in Olvy.

```
GET https://connect.mindcloud.co/v1/universal/olvy/latest/actions/validate-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olvy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/olvy/latest/actions/validate-email?connectionId=$CONNECTION_ID&variables.email=hello%40mindcloud.co" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.email": "hello@mindcloud.co"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/olvy/latest/actions/validate-email?${params}`, {
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
| `variables.email` | string | yes | Email address to validate against Olvy's checker. Example: `hello@mindcloud.co`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "validateEmail": {
          "disposable": true,
          "valid": true
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | GraphQL response envelope. |
| `data.validateEmail` | object | Email validation result. |
| `data.validateEmail.disposable` | boolean | Whether the email uses a disposable inbox. |
| `data.validateEmail.valid` | boolean | Whether the email is valid. |

## Native endpoint

Through the native Olvy API, this operation is `POST /` (base URL `https://app.olvy.co/api/v2/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-email.md) for the provider-specific parameters and requirements.

