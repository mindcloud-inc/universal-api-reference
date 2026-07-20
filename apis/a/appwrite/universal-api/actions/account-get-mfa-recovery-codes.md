# Appwrite: List MFA recovery codes

Retrieves a list of MFA recovery codes from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-get-mfa-recovery-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-get-mfa-recovery-codes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-get-mfa-recovery-codes?${params}`, {
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
      "recoveryCodes": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `recoveryCodes` | array<string> | Recovery codes. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /account/mfa/recovery-codes` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/account-get-mfa-recovery-codes.md) for the provider-specific parameters and requirements.

