# TaxBandits Universal API Examples

These examples use the MindCloud API key and TaxBandits connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test Connection

Retrieves TaxBandits API connection status and version details.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/test-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/test-connection?${params}`, {
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
      "APIVersion": "string",
      "Errors": [
        {}
      ],
      "JWTExpiry": "string",
      "StatusCode": 1,
      "StatusMessage": "string",
      "StatusName": "Ava Chen",
      "TimeZone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Test Connection action reference](actions/test-connection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/taxBandits/latest/actions/test-connection).

## Cancel TIN Matching Request

Cancels a TIN matching request in TaxBandits.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/cancel-tin-matching-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/cancel-tin-matching-request', {
  method: 'PUT',
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
      "ErrorRecords": [
        {}
      ],
      "Errors": [
        {}
      ],
      "SubmissionId": "string",
      "SuccessRecords": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Cancel TIN Matching Request action reference](actions/cancel-tin-matching-request.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/taxBandits/latest/actions/cancel-tin-matching-request).
