# Localazy: List File Keys

Retrieves file keys for a project file in Localazy.

```
GET https://connect.mindcloud.co/v1/universal/localazy/latest/actions/list-file-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Localazy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/localazy/latest/actions/list-file-keys?connectionId=$CONNECTION_ID&projectId=string&fileId=string&lang=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "fileId": "string",
  "lang": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/localazy/latest/actions/list-file-keys?${params}`, {
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
| `projectId` | string | yes | Localazy project id. |
| `fileId` | string | yes | Localazy file id. |
| `lang` | string | yes | Locale code in ll-Scrp-RR format. |
| `deprecated` | boolean | no | Include deprecated keys. |
| `limit` | number | no | Number of keys to return per page. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `next` | string | no | Cursor for the next page of keys. |
| `extraInfo` | boolean | no | Include hidden, limit, deprecated, and comment metadata. |
| `noContent` | boolean | no | Skip translation content values in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "keys": [
        {}
      ],
      "next": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `keys` | array<object> | Paginated list of translation keys and values. |
| `next` | string | Cursor token for the next page, when present. |

## Native endpoint

Through the native Localazy API, this operation is `GET /projects/:projectId/files/:fileId/keys/:lang` (base URL `https://api.localazy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-file-keys.md) for the provider-specific parameters and requirements.

