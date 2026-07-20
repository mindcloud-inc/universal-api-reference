# ID Analyzer Universal API Examples

These examples use the MindCloud API key and ID Analyzer connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List KYC Profiles

Retrieves KYC profiles from ID Analyzer.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/list-kyc-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/list-kyc-profiles?${params}`, {
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

See the full [List KYC Profiles action reference](actions/list-kyc-profiles.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iDAnalyzer/latest/actions/list-kyc-profiles).

## Create a document template

Creates a document template in ID Analyzer.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/create-a-document-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/create-a-document-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string",
    "name": "Ava Chen"
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

See the full [Create a document template action reference](actions/create-a-document-template.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iDAnalyzer/latest/actions/create-a-document-template).
