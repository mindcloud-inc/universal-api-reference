# Close: Merge Leads

Merges two leads in Close.

```
POST https://connect.mindcloud.co/v1/universal/close/latest/actions/merge-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Close `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/close/latest/actions/merge-leads" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destination": "string",
  "source": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/close/latest/actions/merge-leads', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destination": "string",
    "source": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `destination` | string | yes | Destination lead ID for merge. |
| `source` | string | yes | Source lead ID for merge. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Merged lead ID. |

## Native endpoint

Through the native Close API, this operation is `POST /lead/merge/` (base URL `https://api.close.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-leads.md) for the provider-specific parameters and requirements.

