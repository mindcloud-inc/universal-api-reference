# Zendesk: Delete Ticket

Deletes an existing ticket from Zendesk.

```
DELETE https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/delete-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zendesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/delete-ticket?connectionId=$CONNECTION_ID&id=5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/delete-ticket?${params}`, {
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
| `id` | number | yes | Zendesk ticket ID. Example: `5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string",
      "progress": 1,
      "results": [
        {}
      ],
      "status": "string",
      "total": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Job status id. |
| `message` | string | Job status message. |
| `progress` | number | Completed operations in the job. |
| `results[]` | object | Per-item job result rows. |
| `status` | string | Current job status. |
| `total` | number | Total number of operations in the job. |
| `url` | string | URL of the job status resource. |

## Native endpoint

Through the native Zendesk API, this operation is `DELETE /tickets/:id.json` (base URL `https://{{credentials.subdomain}}.zendesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-ticket.md) for the provider-specific parameters and requirements.

