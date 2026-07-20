# Ninox: Get Workspace

Retrieves a workspace from Ninox.

```
GET https://connect.mindcloud.co/v1/universal/ninox/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninox/latest/actions/get-workspace?connectionId=$CONNECTION_ID&teamId=YcHTn3ir8XNSp5EXK" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "YcHTn3ir8XNSp5EXK"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninox/latest/actions/get-workspace?${params}`, {
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
| `teamId` | string | yes | Workspace ID from the List Workspaces action. Example: `YcHTn3ir8XNSp5EXK`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Workspace ID. |
| `name` | string | Workspace name. |

## Native endpoint

Through the native Ninox API, this operation is `GET teams/:teamid` (base URL `https://api.ninox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.

