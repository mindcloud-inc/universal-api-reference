# Listclean: Verify Email Address

Retrieves an email verification result from Listclean.

```
GET https://connect.mindcloud.co/v1/universal/listclean/latest/actions/verify-email-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Listclean `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/listclean/latest/actions/verify-email-address?connectionId=$CONNECTION_ID&email=person%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "person@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/listclean/latest/actions/verify-email-address?${params}`, {
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
| `email` | string | yes | Email address to verify. Example: `person@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "remarks": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Email address that was verified. |
| `remarks` | string | Provider remarks for the verification result. |
| `status` | string | Verification status returned by Listclean. |

## Native endpoint

Through the native Listclean API, this operation is `GET /verify/email/:email` (base URL `https://api.listclean.xyz/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email-address.md) for the provider-specific parameters and requirements.

