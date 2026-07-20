# Leadboxer: Update Lead Tags

Updates lead tags for a lead in Leadboxer.

```
PUT https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/update-lead-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadboxer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/update-lead-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datasetId": "string",
  "leadId": "string",
  "leadTags": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/update-lead-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datasetId": "string",
    "leadId": "string",
    "leadTags": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasetId` | string | yes |  |
| `leadId` | string | yes |  |
| `leadTags` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadboxer API returns.

## Native endpoint

Through the native Leadboxer API, this operation is `PUT /v1/management/lead-tags` (base URL `https://data.leadboxer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead-tags.md) for the provider-specific parameters and requirements.

