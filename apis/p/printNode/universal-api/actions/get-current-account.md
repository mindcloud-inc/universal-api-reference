# PrintNode: Get Current Account

Retrieves current account details from PrintNode.

```
GET https://connect.mindcloud.co/v1/universal/printNode/latest/actions/get-current-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PrintNode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printNode/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printNode/latest/actions/get-current-account?${params}`, {
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
      "canCreateSubAccounts": true,
      "email": "ava@example.com",
      "firstname": "Ava",
      "id": 1,
      "lastname": "Chen",
      "numComputers": 1,
      "permissions": [
        "string"
      ],
      "state": "string",
      "totalPrints": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canCreateSubAccounts` | boolean | Whether the account can create sub-accounts. |
| `email` | string | Account email address. |
| `firstname` | string | Account first name. |
| `id` | number | PrintNode account ID. |
| `lastname` | string | Account last name. |
| `numComputers` | number | Number of computers connected to the account. |
| `permissions` | array<string> | PrintNode permissions granted to the account. |
| `state` | string | Account state. |
| `totalPrints` | number | Total prints processed by the account. |

## Native endpoint

Through the native PrintNode API, this operation is `GET /whoami` (base URL `https://api.printnode.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-account.md) for the provider-specific parameters and requirements.

