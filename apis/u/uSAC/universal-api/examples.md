# USAC Universal API Examples

These examples use the MindCloud API key and USAC connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Datasets



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSAC/latest/actions/list-datasets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uSAC/latest/actions/list-datasets?${params}`, {
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
      "classification": {
        "categories": [
          "string"
        ],
        "domainCategory": "string",
        "domainMetadata": [
          {
            "key": "string",
            "value": "string"
          }
        ],
        "domainTags": [
          "string"
        ]
      },
      "creator": {
        "displayName": "Ava Chen",
        "id": "string",
        "userType": "string"
      },
      "link": "https://example.com",
      "metadata": {
        "domain": "string",
        "license": "string"
      },
      "owner": {
        "displayName": "Ava Chen",
        "id": "string",
        "userType": "string"
      },
      "permalink": "https://example.com",
      "resource": {
        "attribution": "string",
        "attributionLink": "https://example.com",
        "blobMimeType": "string",
        "columnsDatatype": [
          "string"
        ],
        "columnsDescription": [
          "string"
        ],
        "columnsFieldName": [
          "Ava Chen"
        ],
        "columnsFormat": [
          {
            "precision": "string"
          }
        ],
        "columnsName": [
          "Ava Chen"
        ],
        "contactEmail": "ava@example.com",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "dataUpdatedAt": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "downloadCount": 1,
        "hideFromDataJson": true,
        "id": "string",
        "lensDisplayType": "string",
        "lensViewType": "string",
        "locked": true,
        "metadataUpdatedAt": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "pageViews": {
          "pageViewsLastMonth": 1,
          "pageViewsLastMonthLog": 1,
          "pageViewsLastWeek": 1,
          "pageViewsLastWeekLog": 1,
          "pageViewsTotal": 1,
          "pageViewsTotalLog": 1
        },
        "provenance": "string",
        "publicationDate": "2026-05-07T12:00:00.000Z",
        "resourceName": "Ava Chen",
        "type": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

See the full [List Datasets action reference](actions/list-datasets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uSAC/latest/actions/list-datasets).
