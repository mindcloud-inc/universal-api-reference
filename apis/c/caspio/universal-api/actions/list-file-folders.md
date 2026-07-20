# Caspio: List File Folders

Retrieves all file folders from Caspio.

```
GET https://connect.mindcloud.co/v1/universal/caspio/latest/actions/list-file-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caspio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/caspio/latest/actions/list-file-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/caspio/latest/actions/list-file-folders?${params}`, {
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
| `externalKey` | string | no | Optional parent folder ID. |
| `pageNumber` | number | no | Page number. |
| `pageSize` | number | no | Rows per page. |
| `sortField` | string | no | Sort field. |
| `sortDescending` | boolean | no | Set true for descending order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Pagination": {},
      "Result": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Pagination` | object |  |
| `Result` | array<object> |  |

## Native endpoint

Through the native Caspio API, this operation is `GET /v3/files/folders` (base URL `https://d2hbw900.caspio.com/integrations/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-file-folders.md) for the provider-specific parameters and requirements.

