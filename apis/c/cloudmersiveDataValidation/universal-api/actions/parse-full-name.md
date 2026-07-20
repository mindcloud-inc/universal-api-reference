# Cloudmersive Data Validation: Parse Full Name

Parses a full name with Cloudmersive Data Validation.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/parse-full-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Data Validation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/parse-full-name?connectionId=$CONNECTION_ID&input=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/parse-full-name?${params}`, {
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
| `input` | object | yes | Full-name parse and validation request object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "DisplayName": "Ava Chen",
      "FirstName": "Ava",
      "LastName": "Chen",
      "MiddleName": "Ava Chen",
      "NickName": "Ava Chen",
      "Successful": true,
      "Suffix": "string",
      "Title": "string",
      "ValidationResult_FirstName": "Ava",
      "ValidationResult_LastName": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `DisplayName` | string |  |
| `FirstName` | string |  |
| `LastName` | string |  |
| `MiddleName` | string |  |
| `NickName` | string |  |
| `Successful` | boolean |  |
| `Suffix` | string |  |
| `Title` | string |  |
| `ValidationResult_FirstName` | string |  |
| `ValidationResult_LastName` | string |  |

## Native endpoint

Through the native Cloudmersive Data Validation API, this operation is `POST /validate/name/full-name` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-full-name.md) for the provider-specific parameters and requirements.

