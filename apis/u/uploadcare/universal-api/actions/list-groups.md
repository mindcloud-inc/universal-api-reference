# Uploadcare: List Groups

Retrieves all groups from your Uploadcare project.

```
GET https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uploadcare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/list-groups?${params}`, {
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
| `from` | date | no | Start listing groups created after this ISO 8601 timestamp. |
| `ordering` | string | no | Sort order for returned groups. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cdnUrl": "https://example.com",
      "datetimeCreated": "2026-05-07T12:00:00.000Z",
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
| `filesCount` | number | Number of files in the group. |
| `id` | string | Uploadcare group identifier. |
| `url` | string | REST API URL for the group. |

## Native endpoint

Through the native Uploadcare API, this operation is `GET /groups/` (base URL `https://api.uploadcare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

