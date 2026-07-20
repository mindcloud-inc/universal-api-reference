# Shortcut: List Members



```
GET https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/list-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shortcut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/list-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/list-members?${params}`, {
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
| `orgPublicId` | string | no | Limit members to a specific organization. |
| `disabled` | boolean | no | Whether to include disabled members. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "disabled": true,
      "entityType": "string",
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
| `disabled` | boolean |  |
| `entityType` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Shortcut API, this operation is `GET /members` (base URL `https://api.app.shortcut.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-members.md) for the provider-specific parameters and requirements.

