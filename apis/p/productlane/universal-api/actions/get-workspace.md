# Productlane: Get Workspace

Retrieves a workspace from your Productlane account.

```
GET https://connect.mindcloud.co/v1/universal/productlane/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/get-workspace?connectionId=$CONNECTION_ID&id=ba9bf7e6-fc19-40d3-9174-275a63e5fa74" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "ba9bf7e6-fc19-40d3-9174-275a63e5fa74"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productlane/latest/actions/get-workspace?${params}`, {
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
| `id` | string | yes | Workspace ID. Example: `ba9bf7e6-fc19-40d3-9174-275a63e5fa74`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Productlane API returns.

## Native endpoint

Through the native Productlane API, this operation is `GET /workspaces/{id}` (base URL `https://productlane.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.

