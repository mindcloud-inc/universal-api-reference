# Dataway Universal API Examples

These examples use the MindCloud API key and Dataway connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Balance

Retrieves the current vendor balance from Dataway.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataway/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataway/latest/actions/get-balance?${params}`, {
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
      "data": "string",
      "responseCode": "string",
      "responseDescription": "string",
      "responseMessage": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Balance action reference](actions/get-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dataway/latest/actions/get-balance).

## Vend Service

Creates a new vend transaction in Dataway.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dataway/latest/actions/vend-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "service_slug": "string",
  "biller_identifier": "string",
  "amount": "string",
  "reference": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataway/latest/actions/vend-service', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "service_slug": "string",
    "biller_identifier": "string",
    "amount": "string",
    "reference": "string"
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
        "amount": 1,
        "commission": 1,
        "date": "2026-05-07T12:00:00.000Z",
        "externalReference": "string",
        "extras": {},
        "reference": "string",
        "status": "string",
        "title": "string"
      },
      "responseCode": "string",
      "responseDescription": "string",
      "responseMessage": "string"
    }
  ],
  "meta": {}
}
```

See the full [Vend Service action reference](actions/vend-service.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dataway/latest/actions/vend-service).
