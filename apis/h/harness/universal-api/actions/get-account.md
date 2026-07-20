# Harness: Get Account

Retrieves an account from Harness.

```
GET https://connect.mindcloud.co/v1/universal/harness/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harness `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harness/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harness/latest/actions/get-account?${params}`, {
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
      "accountStatus": "string",
      "accountType": "string",
      "cluster": "string",
      "companyName": "Ava Chen",
      "createdAt": 1,
      "defaultExperience": "string",
      "expiryTime": 1,
      "identifier": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountStatus` | string | Harness account status. |
| `accountType` | string | Harness account type. |
| `cluster` | string | Harness cluster. |
| `companyName` | string | Company name for the account. |
| `createdAt` | number | Account creation timestamp in milliseconds. |
| `defaultExperience` | string | Default UI experience. |
| `expiryTime` | number | Trial expiry timestamp in milliseconds. |
| `identifier` | string | Harness account identifier. |
| `name` | string | Harness account name. |

## Native endpoint

Through the native Harness API, this operation is `GET /ng/api/accounts/:accountIdentifier` (base URL `https://app.harness.io/gateway`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

