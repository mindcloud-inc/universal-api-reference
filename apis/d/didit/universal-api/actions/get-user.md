# Didit: Get User

Retrieves a user from Didit.

```
GET https://connect.mindcloud.co/v1/universal/didit/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Didit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/didit/latest/actions/get-user?connectionId=$CONNECTION_ID&vendorData=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vendorData": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/didit/latest/actions/get-user?${params}`, {
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
| `vendorData` | string | yes | Didit user vendor_data identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fullName": "Ava Chen",
      "status": "string",
      "vendorData": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fullName` | string |  |
| `status` | string |  |
| `vendorData` | string |  |

## Native endpoint

Through the native Didit API, this operation is `GET /users/{vendorData}/` (base URL `https://verification.didit.me/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

