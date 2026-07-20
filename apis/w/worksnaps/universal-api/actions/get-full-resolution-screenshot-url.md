# Worksnaps: Get full resolution screenshot URL

Retrieves a full-resolution screenshot URL from Worksnaps.

```
GET https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-full-resolution-screenshot-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worksnaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-full-resolution-screenshot-url?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-full-resolution-screenshot-url?${params}`, {
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
| `project_id` | string | no | ID of the target project |
| `time_entry_id` | string | no | ID of the target Time Entry |

## Response

```json
{
  "success": true,
  "data": [
    {
      "full_resolution_url": "https://example.com",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `full_resolution_url` | string | the URL of the full-resolution screen shot associated with the time entry |
| `id` | number | the ID of the time entry |

## Native endpoint

Through the native Worksnaps API, this operation is `GET /projects/{project_id}/time_entries/{time_entry_id}.xml?full_resolution_url=1` (base URL `https://api.worksnaps.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-full-resolution-screenshot-url.md) for the provider-specific parameters and requirements.

