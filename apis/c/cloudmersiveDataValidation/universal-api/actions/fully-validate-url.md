# Cloudmersive Data Validation: Fully Validate URL

Fully validates a URL with Cloudmersive Data Validation.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/fully-validate-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Data Validation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/fully-validate-url?connectionId=$CONNECTION_ID&request=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "request": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/fully-validate-url?${params}`, {
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
| `request` | object | yes | ValidateUrlRequestFull object containing the URL to validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Valid_Domain": true,
      "Valid_Endpoint": true,
      "Valid_Syntax": true,
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
| `Valid_Domain` | boolean |  |
| `Valid_Endpoint` | boolean |  |
| `Valid_Syntax` | boolean |  |
| `ValidURL` | boolean |  |
| `WellFormedURL` | string |  |

## Native endpoint

Through the native Cloudmersive Data Validation API, this operation is `POST /validate/domain/url/full` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fully-validate-url.md) for the provider-specific parameters and requirements.

