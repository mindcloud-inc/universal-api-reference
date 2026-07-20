# Openlayer: Get Workspace

Retrieves workspace details from the Openlayer API.

```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-workspace?connectionId=$CONNECTION_ID&workspaceId=b9ef2789-e1dd-4946-9ab0-189dcee20750" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "b9ef2789-e1dd-4946-9ab0-189dcee20750"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-workspace?${params}`, {
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
| `workspaceId` | string | yes | Openlayer workspace ID. Default: `b9ef2789-e1dd-4946-9ab0-189dcee20750`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "frameworkCount": 1,
      "id": "string",
      "inviteCount": 1,
      "memberCount": 1,
      "name": "Ava Chen",
      "projectCount": 1,
      "ruleCount": 1,
      "slug": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `frameworkCount` | number |  |
| `id` | string |  |
| `inviteCount` | number |  |
| `memberCount` | number |  |
| `name` | string |  |
| `projectCount` | number |  |
| `ruleCount` | number |  |
| `slug` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Openlayer API, this operation is `GET /workspaces/:workspaceId` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.

