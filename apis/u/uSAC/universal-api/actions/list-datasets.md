# USAC: List Datasets



```
GET https://connect.mindcloud.co/v1/universal/uSAC/latest/actions/list-datasets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a USAC `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `categories` | list | no |  |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classification.categories[]` | string |  |
| `classification.domainCategory` | string |  |
| `classification.domainMetadata[].key` | string |  |
| `classification.domainMetadata[].value` | string |  |
| `classification.domainTags[]` | string |  |
| `creator.displayName` | string |  |
| `creator.id` | string |  |
| `creator.userType` | string |  |
| `link` | string |  |
| `metadata.domain` | string |  |
| `metadata.license` | string |  |
| `owner.displayName` | string |  |
| `owner.id` | string |  |
| `owner.userType` | string |  |
| `permalink` | string |  |
| `resource.attribution` | string |  |
| `resource.attributionLink` | string |  |
| `resource.blobMimeType` | string |  |
| `resource.columnsDatatype[]` | string |  |
| `resource.columnsDescription[]` | string |  |
| `resource.columnsFieldName[]` | string |  |
| `resource.columnsFormat[].precision` | string |  |
| `resource.columnsName[]` | string |  |
| `resource.contactEmail` | string |  |
| `resource.createdAt` | date |  |
| `resource.dataUpdatedAt` | date |  |
| `resource.description` | string |  |
| `resource.downloadCount` | number |  |
| `resource.hideFromDataJson` | boolean |  |
| `resource.id` | string |  |
| `resource.lensDisplayType` | string |  |
| `resource.lensViewType` | string |  |
| `resource.locked` | boolean |  |
| `resource.metadataUpdatedAt` | date |  |
| `resource.name` | string |  |
| `resource.pageViews.pageViewsLastMonth` | number |  |
| `resource.pageViews.pageViewsLastMonthLog` | number |  |
| `resource.pageViews.pageViewsLastWeek` | number |  |
| `resource.pageViews.pageViewsLastWeekLog` | number |  |
| `resource.pageViews.pageViewsTotal` | number |  |
| `resource.pageViews.pageViewsTotalLog` | number |  |
| `resource.provenance` | string |  |
| `resource.publicationDate` | date |  |
| `resource.resourceName` | string |  |
| `resource.type` | string |  |
| `resource.updatedAt` | date |  |

## Native endpoint

Through the native USAC API, this operation is `GET catalog/v1` (base URL `https://opendata.usac.org/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-datasets.md) for the provider-specific parameters and requirements.

