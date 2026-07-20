# Metance: Get Content By ID

Retrieves content from Metance by ID.

```
GET https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-content-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metance `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-content-by-id?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-content-by-id?${params}`, {
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
| `id` | number | yes | Metance content identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answerCount": 1,
      "contentText": "string",
      "contentUrl": "https://example.com",
      "folderName": "Ava Chen",
      "id": 1,
      "name": "Ava Chen",
      "status": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answerCount` | number | Answer count |
| `contentText` | string | Content text |
| `contentUrl` | string | Content URL slug |
| `folderName` | string | Folder name |
| `id` | number | Content ID |
| `name` | string | Content name |
| `status` | number | Content status |
| `title` | string | Content title |

## Native endpoint

Through the native Metance API, this operation is `GET /contents/{id}` (base URL `https://api.metance.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-content-by-id.md) for the provider-specific parameters and requirements.

