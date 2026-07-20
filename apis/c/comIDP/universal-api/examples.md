# ComIDP Universal API Examples

These examples use the MindCloud API key and ComIDP connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Asset Details

Retrieves processed asset details from ComIDP.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/comIDP/latest/actions/get-asset-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/comIDP/latest/actions/get-asset-details?${params}`, {
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

See the full [Get Asset Details action reference](actions/get-asset-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/comIDP/latest/actions/get-asset-details).

## CSV to PDF

Creates a ComIDP job to convert a CSV file to PDF.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/comIDP/latest/actions/csv-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/comIDP/latest/actions/csv-to-pdf', {
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

See the full [CSV to PDF action reference](actions/csv-to-pdf.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/comIDP/latest/actions/csv-to-pdf).
