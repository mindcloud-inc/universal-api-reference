# Storydoc: List Stories

Retrieves stories from Storydoc.

```
GET https://connect.mindcloud.co/v1/universal/storydoc/latest/actions/list-stories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storydoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storydoc/latest/actions/list-stories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storydoc/latest/actions/list-stories?${params}`, {
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
| `status` | list<string> | no | Filter stories by status. One of: `Archived`, `Draft`, `Live`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dynamicVariables": {},
      "id": "string",
      "previewUrl": "https://example.com",
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Timestamp when the story was created. |
| `dynamicVariables` | object | Dynamic variable configuration for the story. Current runtime evidence returned an empty collection for this field. |
| `id` | string | Unique identifier for the story. |
| `previewUrl` | string | Preview URL for the story when available. |
| `status` | string | Current Storydoc status for the story. |
| `title` | string | Title of the story. |

## Native endpoint

Through the native Storydoc API, this operation is `GET /v2/stories` (base URL `https://api.storydoc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stories.md) for the provider-specific parameters and requirements.

