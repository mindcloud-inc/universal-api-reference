# LaunchNotes: Get Work Item



```
GET https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/get-work-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchNotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/get-work-item?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/get-work-item?${params}`, {
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
| `id` | string | yes | Work item identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "content": "string",
      "contentType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the work item is archived. |
| `content` | string | Work item content. |
| `contentType` | string | Work item content type. |
| `createdAt` | date | Work item creation timestamp. |
| `id` | string | Work item identifier. |
| `updatedAt` | date | Work item update timestamp. |

## Native endpoint

Through the native LaunchNotes API, this operation is `POST /graphql` (base URL `https://app.launchnotes.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-work-item.md) for the provider-specific parameters and requirements.

