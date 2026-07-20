# no2bounce Universal API Examples

These examples use the MindCloud API key and no2bounce connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Bulk Validation Status

Retrieves bulk validation status from no2bounce by tracking ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/no2bounce/latest/actions/get-bulk-validation-status?connectionId=$CONNECTION_ID&trackingId=Paste%20the%20tracking%20ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trackingId": "Paste the tracking ID"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/no2bounce/latest/actions/get-bulk-validation-status?${params}`, {
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
      "creditDebited": 1,
      "overallStatus": "string",
      "percent": 1,
      "result": {
        "downloadFile": "string"
      },
      "totalCredit": 1,
      "totalRecord": 1,
      "trackingId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Bulk Validation Status action reference](actions/get-bulk-validation-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/no2bounce/latest/actions/get-bulk-validation-status).

## Submit Bulk Validation

Creates a bulk validation job in no2bounce.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/no2bounce/latest/actions/submit-bulk-validation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailList[]": "Add one or more email addresses"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/no2bounce/latest/actions/submit-bulk-validation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailList[]": "Add one or more email addresses"
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
      "data": {
        "trackingId": "string"
      },
      "message": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

See the full [Submit Bulk Validation action reference](actions/submit-bulk-validation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/no2bounce/latest/actions/submit-bulk-validation).
