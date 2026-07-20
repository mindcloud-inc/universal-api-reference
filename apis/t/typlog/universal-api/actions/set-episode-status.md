# Typlog: Set Episode Status

Updates the status of a Typlog episode.

```
PUT https://connect.mindcloud.co/v1/universal/typlog/latest/actions/set-episode-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typlog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/typlog/latest/actions/set-episode-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1",
  "siteId": "4863"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typlog/latest/actions/set-episode-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "1",
    "siteId": "4863"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the episode. Example: `1`. |
| `siteId` | number | yes | Typlog site ID used to set the X-Site-Id header. Example: `4863`. |
| `status` | string | no | Target episode status. Example: `published`. |
| `publishedAt` | date | no | Publish timestamp for scheduled or published episodes. Example: `2026-03-31T18:00:00Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Updated status returned after changing the episode state. |

## Native endpoint

Through the native Typlog API, this operation is `POST /episodes/[:id]/status` (base URL `https://api.typlog.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-episode-status.md) for the provider-specific parameters and requirements.

