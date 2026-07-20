# Encodian Universal API Examples

These examples use the MindCloud API key and Encodian connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Subscription Status

Retrieves subscription status from Encodian.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/get-subscription-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodian/latest/actions/get-subscription-status?${params}`, {
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
      "availableActionsMonth": 1,
      "availableActionsMonthDec": 1,
      "billingInterval": "string",
      "expiryDate": "string",
      "httpStatusCode": 1,
      "httpStatusMessage": "string",
      "monthlyActions": 1,
      "operationId": {},
      "operationStatus": {},
      "subscriptionEnabled": true,
      "subscriptionLevel": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Subscription Status action reference](actions/get-subscription-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/encodian/latest/actions/get-subscription-status).

## Convert Excel

Converts an Excel file in Encodian.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-excel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "outputFormat": "PDF",
  "filename": "hello.csv",
  "fileContent": "Base64 encoded Excel or CSV file content"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-excel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "outputFormat": "PDF",
    "filename": "hello.csv",
    "fileContent": "Base64 encoded Excel or CSV file content"
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
      "errors": [
        "string"
      ],
      "fileContent": "string",
      "filename": "Ava Chen",
      "httpStatusCode": 1,
      "httpStatusMessage": "string",
      "operationId": "string",
      "operationStatus": "string"
    }
  ],
  "meta": {}
}
```

See the full [Convert Excel action reference](actions/convert-excel.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/encodian/latest/actions/convert-excel).
