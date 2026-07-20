# Unbounce: Retrieve Sub Account

Retrieves details for an Unbounce sub-account.

```
GET https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/retrieve-sub-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unbounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/retrieve-sub-account?connectionId=$CONNECTION_ID&sub_account_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sub_account_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/retrieve-sub-account?${params}`, {
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
| `sub_account_id` | string | yes | Unbounce sub-account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "createdAt": "string",
      "domainsCount": 1,
      "id": "string",
      "metadata": {},
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `createdAt` | string |  |
| `domainsCount` | number |  |
| `id` | string |  |
| `metadata` | object |  |
| `name` | string |  |

## Native endpoint

Through the native Unbounce API, this operation is `GET /sub_accounts/:sub_account_id` (base URL `https://api.unbounce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-sub-account.md) for the provider-specific parameters and requirements.

