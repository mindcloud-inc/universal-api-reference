# Understory: Get Experience

Retrieves an experience from Understory.

```
GET https://connect.mindcloud.co/v1/universal/understory/latest/actions/get-experience
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Understory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/understory/latest/actions/get-experience?connectionId=$CONNECTION_ID&experienceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "experienceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/understory/latest/actions/get-experience?${params}`, {
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
| `experienceId` | string | yes | The unique identifier of the experience. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "media": [
        {
          "mime_type": "string",
          "type": "string",
          "url": "https://example.com"
        }
      ],
      "name": "Ava Chen",
      "state": "string",
      "tag_ids": [
        [
          "string"
        ]
      ],
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `description` | string |  |
| `id` | string |  |
| `media[].mime_type` | string |  |
| `media[].type` | string |  |
| `media[].url` | string |  |
| `name` | string |  |
| `state` | string |  |
| `tag_ids[]` | array<string> |  |
| `type` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Understory API, this operation is `GET /v1/experiences/{{experienceId}}` (base URL `https://api.understory.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-experience.md) for the provider-specific parameters and requirements.

