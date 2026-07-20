# Smartcat: Get Account

Retrieves account details from the current Smartcat account.

```
GET https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartcat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/get-account?${params}`, {
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
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "endCustomerValue": "string",
      "id": "string",
      "interInstallationAccountId": "string",
      "isDisabled": true,
      "isPersonal": true,
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | date | Account creation timestamp |
| `endCustomerValue` | string | Account customer-value segment |
| `id` | string | Smartcat account ID |
| `interInstallationAccountId` | string | Inter-installation account ID |
| `isDisabled` | boolean | Whether the account is disabled |
| `isPersonal` | boolean | Whether the account is personal |
| `name` | string | Account display name |
| `type` | string | Smartcat account type |

## Native endpoint

Through the native Smartcat API, this operation is `GET /api/integration/v1/account` (base URL `https://smartcat.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

