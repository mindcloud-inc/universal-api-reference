# Gridly: Get Branch

Retrieves a branch from Gridly by branch ID.

```
GET https://connect.mindcloud.co/v1/universal/gridly/latest/actions/get-branch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gridly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gridly/latest/actions/get-branch?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gridly/latest/actions/get-branch?${params}`, {
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
| `id` | string | yes | The unique identifier of the branch to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columns": [
        {}
      ],
      "defaultAccessViewId": "string",
      "id": "string",
      "isMaster": true,
      "metadata": {},
      "name": "Ava Chen",
      "recordIdentifierType": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columns` | array<object> | Columns configured in the branch. |
| `defaultAccessViewId` | string | Default view ID for the branch. |
| `id` | string | Branch ID. |
| `isMaster` | boolean | Whether the branch is the master branch. |
| `metadata` | object | Branch metadata. |
| `name` | string | Branch name. |
| `recordIdentifierType` | string | Record identifier strategy. |
| `status` | string | Branch status. |

## Native endpoint

Through the native Gridly API, this operation is `GET /branches/:id` (base URL `https://api.gridly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-branch.md) for the provider-specific parameters and requirements.

