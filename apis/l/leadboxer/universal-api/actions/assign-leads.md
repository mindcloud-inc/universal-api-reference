# Leadboxer: Assign Leads

Assigns a lead to a user in Leadboxer.

```
PUT https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/assign-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadboxer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/assign-leads" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leadId": "string",
  "datasetId": "string",
  "assignee": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/assign-leads', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leadId": "string",
    "datasetId": "string",
    "assignee": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leadId` | string | yes |  |
| `datasetId` | string | yes |  |
| `assignee` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadboxer API returns.

## Native endpoint

Through the native Leadboxer API, this operation is `PUT /v1/management/assign-leads` (base URL `https://data.leadboxer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-leads.md) for the provider-specific parameters and requirements.

