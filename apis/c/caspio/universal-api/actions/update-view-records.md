# Caspio: Update View Records

Updates existing view records in Caspio.

```
PUT https://connect.mindcloud.co/v1/universal/caspio/latest/actions/update-view-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caspio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/caspio/latest/actions/update-view-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "viewName": "Ava Chen",
  "where": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/caspio/latest/actions/update-view-records', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "viewName": "Ava Chen",
    "where": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `viewName` | string | yes | Target view name. |
| `where` | string | yes | SQL-like WHERE clause that selects the rows to update. |
| `response` | string | no | Optional response type. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Caspio API returns.

## Native endpoint

Through the native Caspio API, this operation is `PUT /v3/views/{viewName}/records` (base URL `https://d2hbw900.caspio.com/integrations/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-view-records.md) for the provider-specific parameters and requirements.

