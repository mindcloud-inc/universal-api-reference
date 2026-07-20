# Clio Manage: Get Calendar Entry

Retrieves a calendar entry from Clio Manage by entry ID.

```
GET https://connect.mindcloud.co/v1/universal/clio/latest/actions/get-calendar-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clio Manage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clio/latest/actions/get-calendar-entry?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clio/latest/actions/get-calendar-entry?${params}`, {
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
| `id` | number | yes | The Clio calendar entry ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `etag` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Clio Manage API, this operation is `GET /calendar_entries/:id.json` (base URL `https://app.clio.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-calendar-entry.md) for the provider-specific parameters and requirements.

