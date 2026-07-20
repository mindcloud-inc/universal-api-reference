# Alto: Get Branch

Retrieves a branch from Alto by ID.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-branch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-branch?connectionId=$CONNECTION_ID&branchId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "branchId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-branch?${params}`, {
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
| `branchId` | string | yes | Unique Alto branch identifier. |

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

Through the native Alto API, this operation is `GET /branches/:branchId` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-branch.md) for the provider-specific parameters and requirements.

