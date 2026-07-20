# Abbyy Universal API Examples

These examples use the MindCloud API key and Abbyy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tasks

Retrieves OCR tasks from ABBYY Cloud OCR SDK.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abbyy/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abbyy/latest/actions/list-tasks?${params}`, {
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

See the full [List Tasks action reference](actions/list-tasks.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/abbyy/latest/actions/list-tasks).

## Process Barcode Field

Creates an OCR task for a barcode field in ABBYY.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/abbyy/latest/actions/process-barcode-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/abbyy/latest/actions/process-barcode-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
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

See the full [Process Barcode Field action reference](actions/process-barcode-field.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/abbyy/latest/actions/process-barcode-field).
