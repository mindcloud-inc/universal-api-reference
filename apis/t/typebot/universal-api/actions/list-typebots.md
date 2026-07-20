# Typebot: List Typebots



```
GET https://connect.mindcloud.co/v1/universal/typebot/latest/actions/list-typebots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typebot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typebot/latest/actions/list-typebots?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typebot/latest/actions/list-typebots?${params}`, {
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
| `workspaceId` | string | yes | Workspace ID to list typebots from. |
| `folderId` | string | no | Optional folder ID to filter typebots. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessRight": "string",
      "id": "string",
      "name": "Ava Chen",
      "publishedTypebotId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessRight` | string |  |
| `id` | string |  |
| `name` | string |  |
| `publishedTypebotId` | string |  |

## Native endpoint

Through the native Typebot API, this operation is `GET /v1/typebots` (base URL `https://app.typebot.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-typebots.md) for the provider-specific parameters and requirements.

