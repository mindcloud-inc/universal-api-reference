# Print.one Postcards: List Custom Files

Retrieves custom files from Print.one Postcards.

```
GET https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/list-custom-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Print.one Postcards `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/list-custom-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/list-custom-files?${params}`, {
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
| `search` | string | no | Search term to filter custom files |
| `searchBy` | string | no | Fields to search by |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fileExtension": "string",
      "fileName": "Ava Chen",
      "id": "string",
      "metadata": {
        "height": "string",
        "type": "string",
        "width": "string"
      },
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string |  |
| `createdAt` | date |  |
| `fileExtension` | string |  |
| `fileName` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `metadata.height` | string |  |
| `metadata.type` | string |  |
| `metadata.width` | string |  |
| `size` | number |  |

## Native endpoint

Through the native Print.one Postcards API, this operation is `GET /v2/customfiles` (base URL `https://api.print.one`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-custom-files.md) for the provider-specific parameters and requirements.

