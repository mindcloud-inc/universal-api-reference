# Aspire Universal API Examples

These examples use the MindCloud API key and Aspire connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get API Version

Retrieves the current API version from Aspire.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/get-api-version?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/get-api-version?${params}`, {
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get API Version action reference](actions/get-api-version.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aspire/latest/actions/get-api-version).

## Approve Receipt

Approves an existing Aspire receipt and can optionally receive it at the same time. This is the only post-create update path for a receipt. At approve time, the only receipt fields that can be added or changed are the vendor invoice number and vendor invoice date. No other receipt field can be edited through this action, including notes, extra costs or freight, receipt items, received date, vendor, branch, or work ticket. If the user asks to change a non-invoice-metadata field on an existing receipt, surface that limitation upfront and offer the available path of recreating the receipt with the corrected values.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/approve-receipt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/approve-receipt', {
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
  "data": [],
  "meta": {}
}
```

See the full [Approve Receipt action reference](actions/approve-receipt.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aspire/latest/actions/approve-receipt).
