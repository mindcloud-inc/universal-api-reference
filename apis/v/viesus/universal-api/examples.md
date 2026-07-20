# Viesus Universal API Examples

These examples use the MindCloud API key and Viesus connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves the current account in Viesus.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viesus/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viesus/latest/actions/get-account?${params}`, {
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
      "account": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/viesus/latest/actions/get-account).

## Analyze PDF

Analyzes a PDF upload in Viesus.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/viesus/latest/actions/analyze-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viesus/latest/actions/analyze-pdf', {
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
      "analyzePdf": {}
    }
  ],
  "meta": {}
}
```

See the full [Analyze PDF action reference](actions/analyze-pdf.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/viesus/latest/actions/analyze-pdf).
