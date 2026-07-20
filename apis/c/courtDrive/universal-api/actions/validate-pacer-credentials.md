# Court Drive: Validate PACER Credentials



```
GET https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/validate-pacer-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Court Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/validate-pacer-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/validate-pacer-credentials?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "client_code_format": "string",
      "client_code_message": "string",
      "error_message": "string",
      "has_e_filer_privileges": true,
      "is_client_code_required": true,
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_code_format` | string |  |
| `client_code_message` | string |  |
| `error_message` | string |  |
| `has_e_filer_privileges` | boolean |  |
| `is_client_code_required` | boolean |  |
| `valid` | boolean |  |

## Native endpoint

Through the native Court Drive API, this operation is `POST /pacer/credentials/validate` (base URL `https://v1.courtapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-pacer-credentials.md) for the provider-specific parameters and requirements.

