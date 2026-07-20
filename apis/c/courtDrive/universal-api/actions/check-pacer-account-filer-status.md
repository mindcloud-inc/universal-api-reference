# Court Drive: Check PACER Account Filer Status



```
GET https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/check-pacer-account-filer-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Court Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/check-pacer-account-filer-status?connectionId=$CONNECTION_ID&pacerUser=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pacerUser": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/check-pacer-account-filer-status?${params}`, {
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
| `pacerUser` | string | yes | PACER username to check filer status for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error_description": "string",
      "has_e_filer_privileges": true,
      "is_training": true,
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error_description` | string |  |
| `has_e_filer_privileges` | boolean |  |
| `is_training` | boolean |  |
| `valid` | boolean |  |

## Native endpoint

Through the native Court Drive API, this operation is `POST /pacer/credentials/check-filer-status` (base URL `https://v1.courtapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-pacer-account-filer-status.md) for the provider-specific parameters and requirements.

