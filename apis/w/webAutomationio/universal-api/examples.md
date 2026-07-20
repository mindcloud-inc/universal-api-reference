# WebAutomation.io Universal API Examples

These examples use the MindCloud API key and WebAutomation.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Extractors

Lists all extractors in your WebAutomation account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webAutomationio/latest/actions/list-extractors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webAutomationio/latest/actions/list-extractors?${params}`, {
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

See the full [List Extractors action reference](actions/list-extractors.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/webAutomationio/latest/actions/list-extractors).

## Activate Extractor

Activates a specific extractor for use.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/webAutomationio/latest/actions/activate-extractor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "extractorId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webAutomationio/latest/actions/activate-extractor', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "extractorId": 1
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

See the full [Activate Extractor action reference](actions/activate-extractor.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/webAutomationio/latest/actions/activate-extractor).
