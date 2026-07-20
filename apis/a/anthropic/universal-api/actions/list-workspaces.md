# Anthropic: List Workspaces

Retrieves workspaces in the Anthropic organization.

```
GET https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anthropic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/list-workspaces?${params}`, {
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
| `beforeId` | string | no | Cursor for previous page. |
| `afterId` | string | no | Cursor for next page. |
| `limit` | number | no | Number of records per page. |
| `includeArchived` | boolean | no | Whether to include archived workspaces. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "firstId": "string",
      "hasMore": true,
      "lastId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | List of workspaces. |
| `firstId` | string | First workspace ID in the page. |
| `hasMore` | boolean | Whether more pages are available. |
| `lastId` | string | Last workspace ID in the page. |

## Native endpoint

Through the native Anthropic API, this operation is `GET /v1/organizations/workspaces` (base URL `https://api.anthropic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

