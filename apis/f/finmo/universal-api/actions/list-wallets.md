# Finmo: List Wallets

Retrieves wallets from the Finmo platform.

```
GET https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-wallets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-wallets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-wallets?${params}`, {
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
| `category` | string | no | Filter wallets by category. |
| `createdAt` | string | no | Filter by UTC creation date (YYYY-MM-DD). |
| `startTime` | number | no | Filter from epoch start timestamp. |
| `endTime` | number | no | Filter to epoch end timestamp. |
| `limit` | number | no | Maximum number of records per page. |
| `page` | number | no | Page number to return. |
| `customerId` | string | no | Filter wallets for a specific customer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        [
          {}
        ]
      ],
      "requestId": "string",
      "requestTime": "string",
      "statusCode": 1,
      "statusText": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | array<object> |  |
| `data[].category` | string |  |
| `data[].createdAt` | string |  |
| `data[].customerId` | object |  |
| `data[].deletedAt` | object |  |
| `data[].description` | string |  |
| `data[].isActive` | boolean |  |
| `data[].isDeleted` | boolean |  |
| `data[].metadata` | object |  |
| `data[].orgId` | string |  |
| `data[].scope` | string |  |
| `data[].updatedAt` | string |  |
| `data[].walletAlias` | string |  |
| `data[].walletId` | string |  |
| `data[].webhookUrl` | object |  |
| `requestId` | string |  |
| `requestTime` | string |  |
| `statusCode` | number |  |
| `statusText` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Finmo API, this operation is `GET /wallet` (base URL `https://api.finmo.net/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-wallets.md) for the provider-specific parameters and requirements.

