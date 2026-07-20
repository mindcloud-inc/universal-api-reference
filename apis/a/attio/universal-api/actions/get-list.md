# Attio: Get List

Retrieves a list from Attio.

```
GET https://connect.mindcloud.co/v1/universal/attio/latest/actions/get-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Attio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/attio/latest/actions/get-list?connectionId=$CONNECTION_ID&list=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "list": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/attio/latest/actions/get-list?${params}`, {
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
| `list` | string | yes | The UUID or slug identifying the list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiSlug": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdByActor": {},
      "id": {},
      "name": "Ava Chen",
      "parentObject": [
        "string"
      ],
      "workspaceMemberAccess": [
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
| `apiSlug` | string | API slug for the list. |
| `createdAt` | date | When the list was created. |
| `createdByActor` | object | Actor that created the list. |
| `id` | object | List identifier payload containing workspace and list ids. |
| `name` | string | Display name of the list. |
| `parentObject` | array<string> | Parent object slugs allowed in the list. |
| `workspaceMemberAccess` | array<object> | Workspace member access rules for the list. |

## Native endpoint

Through the native Attio API, this operation is `GET /v2/lists/:list` (base URL `https://api.attio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list.md) for the provider-specific parameters and requirements.

