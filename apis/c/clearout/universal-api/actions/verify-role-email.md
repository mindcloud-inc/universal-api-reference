# Clearout: Verify Role Email

Retrieves role email verification results from Clearout.

```
GET https://connect.mindcloud.co/v1/universal/clearout/latest/actions/verify-role-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clearout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clearout/latest/actions/verify-role-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clearout/latest/actions/verify-role-email?${params}`, {
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
| `email` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timeout` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessAccount": "string",
      "emailAddress": "ava@example.com",
      "timeTaken": 1,
      "verifiedOn": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessAccount` | string |  |
| `emailAddress` | string |  |
| `timeTaken` | number |  |
| `verifiedOn` | string |  |

## Native endpoint

Through the native Clearout API, this operation is `POST /email/verify/role` (base URL `https://api.clearout.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-role-email.md) for the provider-specific parameters and requirements.

