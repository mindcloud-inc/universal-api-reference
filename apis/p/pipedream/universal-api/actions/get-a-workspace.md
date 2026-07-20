# Pipedream: Get a workspace

Retrieves details for a workspace from Pipedream.

```
GET https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-a-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-a-workspace?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-a-workspace?${params}`, {
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
| `workspaceId` | string | yes | The workspace identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dailyCreditsQuota": 1,
      "dailyCreditsUsed": 1,
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "orgname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dailyCreditsQuota` | number |  |
| `dailyCreditsUsed` | number |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `orgname` | string |  |

## Native endpoint

Through the native Pipedream API, this operation is `GET /workspaces/{org_id}` (base URL `https://api.pipedream.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-workspace.md) for the provider-specific parameters and requirements.

