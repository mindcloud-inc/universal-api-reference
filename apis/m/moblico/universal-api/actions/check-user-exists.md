# Moblico: Check User Exists



```
GET https://connect.mindcloud.co/v1/universal/moblico/latest/actions/check-user-exists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moblico `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moblico/latest/actions/check-user-exists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moblico/latest/actions/check-user-exists?${params}`, {
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
| `username` | string | no | Moblico username to check. |
| `phone` | string | no | Phone number to check. |
| `email` | string | no | Email address to check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "statusType": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Moblico status message. |
| `statusType` | number | Moblico status type code. |

## Native endpoint

Through the native Moblico API, this operation is `GET /users/exists` (base URL `https://moblico.net/services/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-user-exists.md) for the provider-specific parameters and requirements.

