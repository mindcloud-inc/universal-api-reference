# Localazy: List Screenshots

Retrieves screenshots from a Localazy project.

```
GET https://connect.mindcloud.co/v1/universal/localazy/latest/actions/list-screenshots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Localazy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/localazy/latest/actions/list-screenshots?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/localazy/latest/actions/list-screenshots?${params}`, {
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
| `projectId` | string | yes | Localazy project identifier or slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "id": "string",
      "metadata": {},
      "ocrData": "string",
      "phrases": [
        "string"
      ],
      "tags": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string | Custom screenshot description. |
| `id` | string | Localazy identifier of the screenshot. |
| `metadata` | object | Custom metadata attached to the screenshot. |
| `ocrData` | string | OCR text extracted from the screenshot when available. |
| `phrases` | array<string> | Assigned source-key identifiers for the screenshot. |
| `tags` | array<string> | Tags attached to the screenshot. |
| `url` | string | Public URL of the screenshot asset. |

## Native endpoint

Through the native Localazy API, this operation is `GET /projects/:projectId/screenshots` (base URL `https://api.localazy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-screenshots.md) for the provider-specific parameters and requirements.

