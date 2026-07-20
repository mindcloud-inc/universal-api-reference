# SEOTakeoff: Trigger Ranking Snapshot



```
POST https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/trigger-ranking-snapshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SEOTakeoff `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/trigger-ranking-snapshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tenantId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/trigger-ranking-snapshot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tenantId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tenantId` | string | yes | Tenant slug to snapshot. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "articles_processed": 1,
      "errors": [
        "string"
      ],
      "keywords_saved": 1,
      "status": "string",
      "tenants_processed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `articles_processed` | number |  |
| `errors` | array<string> |  |
| `keywords_saved` | number |  |
| `status` | string |  |
| `tenants_processed` | number |  |

## Native endpoint

Through the native SEOTakeoff API, this operation is `POST /api/v1/rankings/snapshot` (base URL `https://api.seotakeoff.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-ranking-snapshot.md) for the provider-specific parameters and requirements.

