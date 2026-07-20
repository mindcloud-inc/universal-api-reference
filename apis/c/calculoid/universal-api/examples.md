# Calculoid Universal API Examples

These examples use the MindCloud API key and Calculoid connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Calculator



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/get-calculator?connectionId=$CONNECTION_ID&calculatorId=109359" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "calculatorId": "109359"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/get-calculator?${params}`, {
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
      "alerts": [
        {
          "msg": "string",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Calculator action reference](actions/get-calculator.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/calculoid/latest/actions/get-calculator).

## Copy Calculator



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/copy-calculator" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "calculatorId": "109359"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/copy-calculator', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "calculatorId": "109359"
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
      "alerts": [
        {
          "msg": "string",
          "type": "string"
        }
      ],
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [Copy Calculator action reference](actions/copy-calculator.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/calculoid/latest/actions/copy-calculator).
