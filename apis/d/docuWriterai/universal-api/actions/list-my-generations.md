# DocuWriter.ai: List My Generations



```
GET https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/list-my-generations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuWriter.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/list-my-generations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/list-my-generations?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "filename": "Ava Chen",
      "generatedHtml": "string",
      "generatedMarkdown": "string",
      "generationType": "string",
      "id": 1,
      "source": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the generation was created. |
| `filename` | string | Filename associated with the generation. |
| `generatedHtml` | string | HTML output for the generation. |
| `generatedMarkdown` | string | Markdown output for the generation. |
| `generationType` | string | Provider generation type code after transformation. |
| `id` | number | Generation identifier. |
| `source` | string | Original submitted source code. |

## Native endpoint

Through the native DocuWriter.ai API, this operation is `POST /api/my-generations` (base URL `https://app.docuwriter.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-my-generations.md) for the provider-specific parameters and requirements.

