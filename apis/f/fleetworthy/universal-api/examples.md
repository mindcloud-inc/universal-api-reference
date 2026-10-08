# Fleetworthy Universal API Examples

These examples use the MindCloud API key and Fleetworthy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Download Asset File



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/download-asset-file?connectionId=$CONNECTION_ID&cpFileId=550e8400-e29b-41d4-a716-446655440000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cpFileId": "550e8400-e29b-41d4-a716-446655440000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/download-asset-file?${params}`, {
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

See the full [Download Asset File action reference](actions/download-asset-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fleetworthy/latest/actions/download-asset-file).

## Create Person Regulated Document



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/create-person-regulated-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "regulatedDocumentTypeId": "string",
  "documentDate": "2026-05-07T12:00:00.000Z",
  "regulatedDocumentStatusId": "string",
  "personId": "string",
  "isActive": "true",
  "locationId": "string",
  "objectId": "string",
  "parentObjectId": "string",
  "objectDisplayName": "Ava Chen",
  "setAsPrimary": "true",
  "metaData": "string",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/create-person-regulated-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "regulatedDocumentTypeId": "string",
    "documentDate": "2026-05-07T12:00:00.000Z",
    "regulatedDocumentStatusId": "string",
    "personId": "string",
    "isActive": "true",
    "locationId": "string",
    "objectId": "string",
    "parentObjectId": "string",
    "objectDisplayName": "Ava Chen",
    "setAsPrimary": "true",
    "metaData": "string",
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

See the full [Create Person Regulated Document action reference](actions/create-person-regulated-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fleetworthy/latest/actions/create-person-regulated-document).
