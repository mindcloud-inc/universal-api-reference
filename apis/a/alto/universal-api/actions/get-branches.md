# Alto: Get Branches

Retrieves branch records from your Alto account.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-branches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-branches?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-branches?${params}`, {
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
| `activeOnly` | boolean | no | When true, returns only active branches. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branchId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultMarket": "string",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branchId` | string |  |
| `createdAt` | date |  |
| `defaultMarket` | string |  |
| `modifiedAt` | date |  |
| `name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Alto API, this operation is `GET /branches` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-branches.md) for the provider-specific parameters and requirements.

