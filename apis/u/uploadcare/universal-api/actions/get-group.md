# Uploadcare: Get Group

Retrieves a group record from Uploadcare.

```
GET https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/get-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uploadcare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/get-group?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/get-group?${params}`, {
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
| `uuid` | string | yes | Uploadcare group UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cdnUrl": "https://example.com",
      "datetimeCreated": "2026-05-07T12:00:00.000Z",
      "files": [
        {}
      ],
      "filesCount": 1,
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cdnUrl` | string | CDN URL for the group. |
| `datetimeCreated` | date | Timestamp when the group was created. |
| `files` | array<object> | Files currently contained in the group. |
| `filesCount` | number | Number of files in the group. |
| `id` | string | Uploadcare group identifier. |
| `url` | string | REST API URL for the group. |

## Native endpoint

Through the native Uploadcare API, this operation is `GET /groups/:uuid/` (base URL `https://api.uploadcare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group.md) for the provider-specific parameters and requirements.

