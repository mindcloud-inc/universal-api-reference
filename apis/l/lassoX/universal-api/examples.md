# Lasso X Universal API Examples

These examples use the MindCloud API key and Lasso X connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Reporting Batches

Retrieves reporting batches from Lasso X.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/list-reporting-batches?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/list-reporting-batches?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "archived": true,
          "batchSize": 1,
          "completionPercentage": 1,
          "emailFormat": "ava@example.com",
          "id": "string",
          "name": "Ava Chen",
          "notificationEmail": "ava@example.com",
          "notificationWebHookUrl": "https://example.com",
          "scheduledTime": "2026-05-07T12:00:00.000Z",
          "status": "string",
          "timestamp": "2026-05-07T12:00:00.000Z",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Reporting Batches action reference](actions/list-reporting-batches.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lassoX/latest/actions/list-reporting-batches).

## Create Reporting Batch

Creates a reporting batch in Lasso X.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/create-reporting-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "batch_name": "Ava Chen",
  "type": "string",
  "format": "string",
  "items[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/create-reporting-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "batch_name": "Ava Chen",
    "type": "string",
    "format": "string",
    "items[]": [{}]
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "batchSize": 1,
      "completionPercentage": 1,
      "emailFormat": "ava@example.com",
      "id": "string",
      "lassoOrgId": "string",
      "lassoUserId": "string",
      "name": "Ava Chen",
      "notificationEmail": "ava@example.com",
      "notificationWebHookUrl": "https://example.com",
      "scheduledTime": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Reporting Batch action reference](actions/create-reporting-batch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lassoX/latest/actions/create-reporting-batch).
