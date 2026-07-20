# DocuWriter.ai: List Generations



```
GET https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/list-generations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuWriter.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/list-generations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/list-generations?${params}`, {
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
      "generated": "string",
      "generatedByUserEmail": "ava@example.com",
      "generationType": "string",
      "tag": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
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
| `generated` | string | Generated output content. |
| `generatedByUserEmail` | string | Email of the generating user. |
| `generationType` | string | Provider generation type code after transformation. |
| `tag` | string | Optional provider tag. |
| `updatedAt` | date | When the generation was last updated. |
| `uuid` | string | Generation UUID. |

## Native endpoint

Through the native DocuWriter.ai API, this operation is `GET /api/generations` (base URL `https://app.docuwriter.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-generations.md) for the provider-specific parameters and requirements.

