# Leadboxer Universal API Examples

These examples use the MindCloud API key and Leadboxer connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Custom Tracking Domain

Retrieves custom tracking domains for a dataset in Leadboxer.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/get-custom-tracking-domain?connectionId=$CONNECTION_ID&datasetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datasetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/get-custom-tracking-domain?${params}`, {
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

See the full [Get Custom Tracking Domain action reference](actions/get-custom-tracking-domain.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/leadboxer/latest/actions/get-custom-tracking-domain).

## Add Custom Tracking Domain

Creates a custom tracking domain in Leadboxer and starts certificate generation.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/add-custom-tracking-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ctd": "string",
  "datasetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/add-custom-tracking-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ctd": "string",
    "datasetId": "string"
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

See the full [Add Custom Tracking Domain action reference](actions/add-custom-tracking-domain.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/leadboxer/latest/actions/add-custom-tracking-domain).
