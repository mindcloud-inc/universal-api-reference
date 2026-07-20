# Grist Universal API Examples

These examples use the MindCloud API key and Grist connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Document

Retrieves a document from Grist.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grist/latest/actions/get-document?connectionId=$CONNECTION_ID&docId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grist/latest/actions/get-document?${params}`, {
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
      "access": "string",
      "aliases": [
        {
          "createdAt": "string",
          "docId": "string",
          "orgId": 1,
          "urlId": "https://example.com"
        }
      ],
      "createdAt": "string",
      "id": "string",
      "isPinned": true,
      "name": "Ava Chen",
      "trunkId": {},
      "type": {},
      "updatedAt": "string",
      "urlId": "https://example.com",
      "workspace": {
        "access": "string",
        "createdAt": "string",
        "id": 1,
        "isSupportWorkspace": true,
        "name": "Ava Chen",
        "org": {
          "access": "string",
          "billingAccount": {
            "externalId": {},
            "externalOptions": {},
            "features": {},
            "id": 1,
            "individual": true,
            "inGoodStanding": true,
            "paymentLink": {},
            "product": {
              "features": {
                "baseMaxApiUnitsPerDocumentPerDay": 1,
                "baseMaxAssistantCalls": 1,
                "baseMaxAttachmentsBytesPerDocument": 1,
                "baseMaxDataSizePerDocument": 1,
                "baseMaxRowsPerDocument": 1,
                "gracePeriodDays": 1,
                "maxAttachmentsBytesPerOrg": 1,
                "maxSharesPerDoc": 1,
                "maxSharesPerWorkspace": 1,
                "snapshotWindow": {
                  "count": 1,
                  "unit": "string"
                },
                "workspaces": true
              },
              "id": 1,
              "name": "Ava Chen"
            },
            "status": {},
            "stripePlanId": {}
          },
          "createdAt": "string",
          "domain": "string",
          "host": {},
          "id": 1,
          "name": "Ava Chen",
          "owner": {
            "createdAt": "string",
            "id": 1,
            "name": "Ava Chen",
            "picture": {},
            "ref": "string",
            "type": "string"
          },
          "updatedAt": "string"
        },
        "owner": {
          "createdAt": "string",
          "id": 1,
          "name": "Ava Chen",
          "picture": {},
          "ref": "string",
          "type": "string"
        },
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Document action reference](actions/get-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/grist/latest/actions/get-document).

## Add Columns

Creates new columns in a Grist table.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/grist/latest/actions/add-columns" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "docId": "string",
  "tableId": "string",
  "columns": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grist/latest/actions/add-columns', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "docId": "string",
    "tableId": "string",
    "columns": "string"
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
      "columns": [
        {
          "id": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Columns action reference](actions/add-columns.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/grist/latest/actions/add-columns).
