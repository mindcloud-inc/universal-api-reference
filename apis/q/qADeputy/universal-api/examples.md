# QADeputy Universal API Examples

These examples use the MindCloud API key and QADeputy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Products

Retrieves products from QADeputy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/list-products?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "name": "Ava Chen",
      "productId": 1,
      "testSuitesCount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Products action reference](actions/list-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/qADeputy/latest/actions/list-products).

## Create Test Result

Creates a test result for a QADeputy test case.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/create-test-result" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "testCaseId": 1,
  "testCaseStatus": 1,
  "createdByUserId": 1,
  "testRun": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/create-test-result', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "testCaseId": 1,
    "testCaseStatus": 1,
    "createdByUserId": 1,
    "testRun": 1
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
      "actualResult": "string",
      "createdBy": "string",
      "testCaseId": "string",
      "testCaseName": "Ava Chen",
      "testCaseStatus": "string",
      "testRun": {
        "name": "Ava Chen",
        "testRunId": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Test Result action reference](actions/create-test-result.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/qADeputy/latest/actions/create-test-result).
