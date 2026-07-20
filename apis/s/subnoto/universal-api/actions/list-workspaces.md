# Subnoto: List Workspaces



```
GET https://connect.mindcloud.co/v1/universal/subnoto/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Subnoto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/subnoto/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/subnoto/latest/actions/list-workspaces?${params}`, {
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
| `page` | number | no | The page number to return. Defaults to 1. Default: `1`. |
| `limit` | number | no | The number of workspaces to return per page. Defaults to 50 and cannot exceed 50. Default: `50`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {},
      "workspaces": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination` | object | Pagination metadata for the workspace list response. |
| `workspaces` | array<object> | The workspaces the authenticated API key owner is a member of. |

## Native endpoint

Through the native Subnoto API, this operation is `POST /public/workspace/list` (base URL `https://app.subnoto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

