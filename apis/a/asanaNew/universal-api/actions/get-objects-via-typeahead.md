# Asana: Get objects via typeahead

Finds objects in Asana by typeahead.

```
GET https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-objects-via-typeahead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-objects-via-typeahead?connectionId=$CONNECTION_ID&workspaceGid=string&resourceType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceGid": "string",
  "resourceType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-objects-via-typeahead?${params}`, {
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
| `workspaceGid` | string | yes |  |
| `resourceType` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | no |  |
| `query` | string | no |  |
| `count` | number | no |  |
| `optPretty` | boolean | no |  |
| `optFields` | list<string> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Asana API returns.

## Native endpoint

Through the native Asana API, this operation is `GET workspaces/:workspace_gid/typeahead` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-objects-via-typeahead.md) for the provider-specific parameters and requirements.

