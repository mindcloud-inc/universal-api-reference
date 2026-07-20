# Frameshift: Create Project

Creates a new project in Frameshift.

```
POST https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frameshift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the project to create |
| `reference` | string | no | The reference genome for the project. Required unless is_collection is true. |
| `description` | string | no | The details surrounding the project being created |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "description": "string",
      "id": 1,
      "isCollection": true,
      "name": "Ava Chen",
      "nickname": {},
      "phiName": {},
      "primarySampleId": {},
      "projectAnnotations": [
        {
          "annotationId": 1,
          "createdAt": "string",
          "id": 1,
          "projectId": 1,
          "updatedAt": "string"
        }
      ],
      "projectAttributes": [
        {
          "attributeId": 1,
          "createdAt": "string",
          "id": 1,
          "projectId": 1,
          "updatedAt": "string"
        }
      ],
      "projectClientApplications": [
        {
          "clientApplicationId": 1,
          "createdAt": "string",
          "id": 1,
          "isActive": true,
          "projectId": 1,
          "updatedAt": "string"
        }
      ],
      "projectDashboard": [
        {
          "attributeId": {},
          "chartId": {},
          "id": 1,
          "isActive": true,
          "isDefault": true,
          "projectAnalysisId": {},
          "projectConversationId": {},
          "projectId": 1,
          "shouldShowNameInBadge": true,
          "type": "string",
          "variantSetId": {},
          "viewOrder": 1
        }
      ],
      "projectSampleAttributes": [
        {
          "attributeId": 1,
          "createdAt": "string",
          "id": 1,
          "projectId": 1,
          "updatedAt": "string"
        }
      ],
      "projectSettings": {
        "canDownloadFiles": true,
        "collectionsTablePagination": {},
        "createdAt": "string",
        "enablePedigrees": true,
        "enableVariantView": true,
        "externalUrl": {},
        "externalUrlAnchorText": {},
        "id": 1,
        "isArchived": true,
        "isDefault": true,
        "isTemplate": true,
        "privacyLevel": "string",
        "projectId": 1,
        "redcapUrl": {},
        "reference": "string",
        "restoreRequested": true,
        "selectedCollectionsTableColumns": [
          "string"
        ],
        "selectedGeneAnnotationIds": {},
        "selectedSampleAttributeChartData": {
          "chartIds": [
            1
          ]
        },
        "selectedSampleAttributeColumnIds": [
          1
        ],
        "selectedVariantAnnotationVersionIds": {},
        "sortedAnnotations": {},
        "templateProjectIds": [
          1
        ],
        "updatedAt": "string",
        "variantsLoadedDescription": {},
        "webhookUrl": {}
      },
      "roles": [
        {
          "canDownload": true,
          "canLaunchApp": true,
          "createdAt": "string",
          "expiryDate": {},
          "id": 1,
          "projectId": 1,
          "roleTypeId": 1,
          "strictSearch": true,
          "updatedAt": "string",
          "userId": 1
        }
      ],
      "uid": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `description` | string |  |
| `id` | number |  |
| `isCollection` | boolean |  |
| `name` | string |  |
| `nickname` | object |  |
| `phiName` | object |  |
| `primarySampleId` | object |  |
| `projectAnnotations[].annotationId` | number |  |
| `projectAnnotations[].createdAt` | string |  |
| `projectAnnotations[].id` | number |  |
| `projectAnnotations[].projectId` | number |  |
| `projectAnnotations[].updatedAt` | string |  |
| `projectAttributes[].attributeId` | number |  |
| `projectAttributes[].createdAt` | string |  |
| `projectAttributes[].id` | number |  |
| `projectAttributes[].projectId` | number |  |
| `projectAttributes[].updatedAt` | string |  |
| `projectClientApplications[].clientApplicationId` | number |  |
| `projectClientApplications[].createdAt` | string |  |
| `projectClientApplications[].id` | number |  |
| `projectClientApplications[].isActive` | boolean |  |
| `projectClientApplications[].projectId` | number |  |
| `projectClientApplications[].updatedAt` | string |  |
| `projectDashboard[].attributeId` | object |  |
| `projectDashboard[].chartId` | object |  |
| `projectDashboard[].id` | number |  |
| `projectDashboard[].isActive` | boolean |  |
| `projectDashboard[].isDefault` | boolean |  |
| `projectDashboard[].projectAnalysisId` | object |  |
| `projectDashboard[].projectConversationId` | object |  |
| `projectDashboard[].projectId` | number |  |
| `projectDashboard[].shouldShowNameInBadge` | boolean |  |
| `projectDashboard[].type` | string |  |
| `projectDashboard[].variantSetId` | object |  |
| `projectDashboard[].viewOrder` | number |  |
| `projectSampleAttributes[].attributeId` | number |  |
| `projectSampleAttributes[].createdAt` | string |  |
| `projectSampleAttributes[].id` | number |  |
| `projectSampleAttributes[].projectId` | number |  |
| `projectSampleAttributes[].updatedAt` | string |  |
| `projectSettings.canDownloadFiles` | boolean |  |
| `projectSettings.collectionsTablePagination` | object |  |
| `projectSettings.createdAt` | string |  |
| `projectSettings.enablePedigrees` | boolean |  |
| `projectSettings.enableVariantView` | boolean |  |
| `projectSettings.externalUrl` | object |  |
| `projectSettings.externalUrlAnchorText` | object |  |
| `projectSettings.id` | number |  |
| `projectSettings.isArchived` | boolean |  |
| `projectSettings.isDefault` | boolean |  |
| `projectSettings.isTemplate` | boolean |  |
| `projectSettings.privacyLevel` | string |  |
| `projectSettings.projectId` | number |  |
| `projectSettings.redcapUrl` | object |  |
| `projectSettings.reference` | string |  |
| `projectSettings.restoreRequested` | boolean |  |
| `projectSettings.selectedCollectionsTableColumns[]` | string |  |
| `projectSettings.selectedGeneAnnotationIds` | object |  |
| `projectSettings.selectedSampleAttributeChartData.chartIds[]` | number |  |
| `projectSettings.selectedSampleAttributeColumnIds[]` | number |  |
| `projectSettings.selectedVariantAnnotationVersionIds` | object |  |
| `projectSettings.sortedAnnotations` | object |  |
| `projectSettings.templateProjectIds[]` | number |  |
| `projectSettings.updatedAt` | string |  |
| `projectSettings.variantsLoadedDescription` | object |  |
| `projectSettings.webhookUrl` | object |  |
| `roles[].canDownload` | boolean |  |
| `roles[].canLaunchApp` | boolean |  |
| `roles[].createdAt` | string |  |
| `roles[].expiryDate` | object |  |
| `roles[].id` | number |  |
| `roles[].projectId` | number |  |
| `roles[].roleTypeId` | number |  |
| `roles[].strictSearch` | boolean |  |
| `roles[].updatedAt` | string |  |
| `roles[].userId` | number |  |
| `uid` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Frameshift API, this operation is `POST /v1/projects` (base URL `https://mosaic.frameshift.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

