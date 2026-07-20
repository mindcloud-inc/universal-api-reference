# Backendless: List Root Directory

Retrieves the root directory listing from Backendless.

```
GET https://connect.mindcloud.co/v1/universal/backendless/latest/actions/list-root-directory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Backendless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/backendless/latest/actions/list-root-directory?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/backendless/latest/actions/list-root-directory?${params}`, {
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
      "createdOn": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "publicUrl": "https://example.com",
      "updatedOn": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | date |  |
| `name` | string |  |
| `publicUrl` | string |  |
| `updatedOn` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Backendless API, this operation is `GET /{{credentials.applicationId}}/{{credentials.apiKey}}/files/` (base URL `{{credentials.apiUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-root-directory.md) for the provider-specific parameters and requirements.

