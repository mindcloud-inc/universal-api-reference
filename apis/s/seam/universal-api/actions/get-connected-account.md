# Seam: Get Connected Account

Retrieves a connected account from Seam.

```
GET https://connect.mindcloud.co/v1/universal/seam/latest/actions/get-connected-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seam/latest/actions/get-connected-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seam/latest/actions/get-connected-account?${params}`, {
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
| `connectedAccountId` | string | no | ID of the connected account that you want to get. |
| `email` | string | no | Email address associated with the connected account that you want to get. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptedCapabilities": [
        "string"
      ],
      "accountType": "string",
      "accountTypeDisplayName": "Ava Chen",
      "automaticallyManageNewDevices": true,
      "connectedAccountId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customMetadata": {},
      "displayName": "Ava Chen",
      "errors": [
        {}
      ],
      "imageUrl": "https://example.com",
      "userIdentifier": {},
      "warnings": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptedCapabilities` | array<string> |  |
| `accountType` | string |  |
| `accountTypeDisplayName` | string |  |
| `automaticallyManageNewDevices` | boolean |  |
| `connectedAccountId` | string |  |
| `createdAt` | date |  |
| `customMetadata` | object |  |
| `displayName` | string |  |
| `errors` | array<object> |  |
| `imageUrl` | string |  |
| `userIdentifier` | object |  |
| `warnings` | array<object> |  |

## Native endpoint

Through the native Seam API, this operation is `POST /connected_accounts/get` (base URL `https://connect.getseam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-connected-account.md) for the provider-specific parameters and requirements.

