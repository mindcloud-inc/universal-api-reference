# DocuWriter.ai: List Spaces



```
GET https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/list-spaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuWriter.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/list-spaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/list-spaces?${params}`, {
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
      "id": 1,
      "isPublic": true,
      "itemsCount": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | ISO-8601 timestamp when the Space was created. |
| `id` | number | Unique identifier of the Space. |
| `isPublic` | boolean | Whether the Space is public. |
| `itemsCount` | number | Number of documents currently in the Space. |
| `name` | string | Name of the Space. |

## Native endpoint

Through the native DocuWriter.ai API, this operation is `GET /api/spaces` (base URL `https://app.docuwriter.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-spaces.md) for the provider-specific parameters and requirements.

