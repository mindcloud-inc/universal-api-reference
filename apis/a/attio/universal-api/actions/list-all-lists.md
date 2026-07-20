# Attio: List All Lists

Retrieves lists from Attio.

```
GET https://connect.mindcloud.co/v1/universal/attio/latest/actions/list-all-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Attio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/attio/latest/actions/list-all-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/attio/latest/actions/list-all-lists?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Attio API, this operation is `GET /v2/lists` (base URL `https://api.attio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-lists.md) for the provider-specific parameters and requirements.

