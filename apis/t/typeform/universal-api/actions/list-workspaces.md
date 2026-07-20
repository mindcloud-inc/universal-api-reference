# Typeform: List Workspaces



```
GET https://connect.mindcloud.co/v1/universal/typeform/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeform `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeform/latest/actions/list-workspaces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typeform/latest/actions/list-workspaces?${params}`, {
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
| `search` | string | no | Filter workspaces by name text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "default": true,
      "forms": {
        "count": 1,
        "href": "string"
      },
      "id": "string",
      "name": "Ava Chen",
      "self": {
        "href": "string"
      },
      "shared": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string | Typeform account ID. |
| `default` | boolean | Whether this is the default workspace. |
| `forms` | object | Workspace forms metadata. |
| `forms.count` | number | Number of forms in workspace. |
| `forms.href` | string | Workspace forms API URL. |
| `id` | string | Workspace ID. |
| `name` | string | Workspace name. |
| `self` | object | Workspace self link object. |
| `self.href` | string | Workspace self URL. |
| `shared` | boolean | Whether the workspace is shared. |

## Native endpoint

Through the native Typeform API, this operation is `GET /workspaces` (base URL `https://api.typeform.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

