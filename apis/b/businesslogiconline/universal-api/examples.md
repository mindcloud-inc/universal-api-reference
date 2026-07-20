# Businesslogic.online Universal API Examples

These examples use the MindCloud API key and Businesslogic.online connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Describe Calculator

Retrieves calculator input and output schemas from Businesslogic.online.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/businesslogiconline/latest/actions/describe-calculator?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/businesslogiconline/latest/actions/describe-calculator?${params}`, {
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
      "available_data": {},
      "expected_input": {},
      "expected_output": {},
      "name": "Ava Chen",
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [Describe Calculator action reference](actions/describe-calculator.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/businesslogiconline/latest/actions/describe-calculator).

## Execute Calculator

Executes a calculator with input values in Businesslogic.online.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/businesslogiconline/latest/actions/execute-calculator" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/businesslogiconline/latest/actions/execute-calculator', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "doubled_value": 1
    }
  ],
  "meta": {}
}
```

See the full [Execute Calculator action reference](actions/execute-calculator.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/businesslogiconline/latest/actions/execute-calculator).
