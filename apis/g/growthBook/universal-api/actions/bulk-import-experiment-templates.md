# GrowthBook: Bulk create or update experiment templates

Bulk creates or updates experiment templates in GrowthBook.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/bulk-import-experiment-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/bulk-import-experiment-templates" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templates[]": [
    "sample"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/bulk-import-experiment-templates', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templates[]": ["sample"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templates[]` | array<object> | yes | Default: `["sample"]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "added": 1,
      "updated": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `added` | number |  |
| `updated` | number |  |

## Native endpoint

Through the native GrowthBook API, this operation is `POST /experiment-templates/bulk-import` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-import-experiment-templates.md) for the provider-specific parameters and requirements.

