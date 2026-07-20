# Verificaremails: Validate Single Email Input

Retrieves an email validation result from Verificaremails.

```
GET https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/validate-single-email-input
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verificaremails `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/validate-single-email-input?connectionId=$CONNECTION_ID&term=test%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "term": "test@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/validate-single-email-input?${params}`, {
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
| `term` | string | yes | Email address to validate. Provide a single email string. Example: `test@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "requestId": "string",
      "result": {},
      "resultCode": "string",
      "resultType": "string",
      "term": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Validation record identifier returned by Verificaremails. |
| `requestId` | string | Provider request identifier for this validation. |
| `result` | object | Service-specific validation details returned by the provider. |
| `resultCode` | string | Provider result code for the validation outcome. |
| `resultType` | string | Human-readable validation outcome from the provider. |
| `term` | string | Input term that was validated. |

## Native endpoint

Through the native Verificaremails API, this operation is `GET /email/validate/single` (base URL `https://dashboard.verificaremails.com/myapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-single-email-input.md) for the provider-specific parameters and requirements.

