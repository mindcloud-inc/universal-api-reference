# Airiam AI: List Experts

Retrieves a list of experts from Airiam AI.

```
GET https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/list-experts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airiam AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/list-experts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/list-experts?${params}`, {
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
| `showPublic` | boolean | no | Whether to include public experts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "isPublic": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Description of the Plus entry. |
| `id` | string | Unique identifier for the Plus entry. |
| `isPublic` | boolean | Whether the entry is public. |
| `title` | string | Title of the Plus entry. |

## Native endpoint

Through the native Airiam AI API, this operation is `GET /api/v1/plus` (base URL `https://platform.sectorflow.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-experts.md) for the provider-specific parameters and requirements.

