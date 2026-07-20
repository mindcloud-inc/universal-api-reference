# EzzyCRM Universal API Examples

These examples use the MindCloud API key and EzzyCRM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ezzyCRM/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ezzyCRM/latest/actions/list-users?${params}`, {
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
      "emailAddress": "ava@example.com",
      "firstName": "Ava",
      "isActive": "string",
      "lastName": "Chen",
      "userId": 1
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ezzyCRM/latest/actions/list-users).

## Create Lead



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ezzyCRM/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactModel.firstName": "Ava",
  "contactModel.lastName": "Chen",
  "organizationModel.organizationName": "Ava Chen",
  "userId": 1,
  "dealTitle": "string",
  "dealCurrencyId": 1,
  "pipelineId": 1,
  "stageCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ezzyCRM/latest/actions/create-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactModel.firstName": "Ava",
    "contactModel.lastName": "Chen",
    "organizationModel.organizationName": "Ava Chen",
    "userId": 1,
    "dealTitle": "string",
    "dealCurrencyId": 1,
    "pipelineId": 1,
    "stageCode": "string"
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
      "accountId": 1,
      "dealId": 1,
      "dealTitle": "string",
      "dealValue": "string",
      "pipelineId": 1,
      "userId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Lead action reference](actions/create-lead.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ezzyCRM/latest/actions/create-lead).
