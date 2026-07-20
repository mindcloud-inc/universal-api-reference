# Cloudmersive Data Validation: Validate URL Syntax

Validates URL syntax with Cloudmersive Data Validation.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/validate-url-syntax
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Data Validation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/validate-url-syntax?connectionId=$CONNECTION_ID&request=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "request": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/validate-url-syntax?${params}`, {
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
| `request` | object | yes | ValidateUrlRequestSyntaxOnly object, for example {"URL":"https://cloudmersive.com"}. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "TopLevelDomainName": "Ava Chen",
      "ValidURL": true,
      "WellFormedURL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `TopLevelDomainName` | string |  |
| `ValidURL` | boolean |  |
| `WellFormedURL` | string |  |

## Native endpoint

Through the native Cloudmersive Data Validation API, this operation is `POST /validate/domain/url/syntax-only` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-url-syntax.md) for the provider-specific parameters and requirements.

