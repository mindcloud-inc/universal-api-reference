# Sage Intacct Universal API Examples

These examples use the MindCloud API key and Sage Intacct connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check GLBATCH Duplicate



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intacct/latest/actions/check-glbatch-duplicate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intacct/latest/actions/check-glbatch-duplicate?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Check GLBATCH Duplicate action reference](actions/check-glbatch-duplicate.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/intacct/latest/actions/check-glbatch-duplicate).

## Create Budget



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-budget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "budgetId": "2019 Annual Plan",
  "description": "string",
  "periodName": "Month Ended January 2019",
  "budgetItems[]": [
    "string"
  ],
  "budgetItems[].accountNo": "string",
  "budgetItems[].amount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-budget', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "budgetId": "2019 Annual Plan",
    "description": "string",
    "periodName": "Month Ended January 2019",
    "budgetItems[]": ["string"],
    "budgetItems[].accountNo": "string",
    "budgetItems[].amount": 1
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
      "budgetId": "string",
      "response": {},
      "sageRecordNo": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Budget action reference](actions/create-budget.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/intacct/latest/actions/create-budget).
