# LOBSTR.IO: Get Account Details

Retrieves account details from LOBSTR.IO.

```
GET https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/get-account-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LOBSTR.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/get-account-details?connectionId=$CONNECTION_ID&accountHash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountHash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/get-account-details?${params}`, {
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
| `accountHash` | string | yes | The unique identifier (hash) of the account. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountTypeHash": "string",
      "baseurl": "https://example.com",
      "cookies": [
        {}
      ],
      "createdAt": "string",
      "icon": "string",
      "id": "string",
      "lastSynchronizationTime": "string",
      "object": "string",
      "params": {},
      "squids": [
        {}
      ],
      "status": "string",
      "statusCodeDescription": "string",
      "statusCodeInfo": "string",
      "type": "string",
      "updatedAt": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountTypeHash` | string |  |
| `baseurl` | string |  |
| `cookies` | array<object> |  |
| `createdAt` | string |  |
| `icon` | string |  |
| `id` | string |  |
| `lastSynchronizationTime` | string |  |
| `object` | string |  |
| `params` | object |  |
| `squids` | array<object> |  |
| `status` | string |  |
| `statusCodeDescription` | string |  |
| `statusCodeInfo` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `username` | string |  |

## Native endpoint

Through the native LOBSTR.IO API, this operation is `GET /v1/accounts/:account_hash` (base URL `https://api.lobstr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-details.md) for the provider-specific parameters and requirements.

