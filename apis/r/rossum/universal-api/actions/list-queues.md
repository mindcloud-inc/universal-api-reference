# Rossum: List Queues

Retrieves queues from Rossum.

```
GET https://connect.mindcloud.co/v1/universal/rossum/latest/actions/list-queues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/list-queues?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rossum/latest/actions/list-queues?${params}`, {
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
| `ordering` | string | no | Ordering expression, for example name or -name. |
| `workspace` | number | no | Filter queues by Rossum workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "next": {},
        "previous": {}
      },
      "results": [
        {
          "archiveEnabled": true,
          "automationEnabled": true,
          "automationLevel": "string",
          "connector": {},
          "counts": {
            "confirmed": 1,
            "created": 1,
            "deleted": 1,
            "exported": 1,
            "exporting": 1,
            "failedExport": 1,
            "failedImport": 1,
            "importing": 1,
            "inWorkflow": 1,
            "postponed": 1,
            "purged": 1,
            "rejected": 1,
            "reviewing": 1,
            "split": 1,
            "toReview": 1
          },
          "dedicatedEngine": {},
          "defaultScoreThreshold": 1,
          "deleteAfter": {},
          "documentLifetime": {},
          "engine": "string",
          "genericEngine": {},
          "id": 1,
          "inbox": "string",
          "locale": "string",
          "metadata": {
            "queueTemplate": "string"
          },
          "modifiedAt": "string",
          "modifiedBy": {},
          "name": "Ava Chen",
          "qualitySpotCheckPercentage": 1,
          "rirParams": {},
          "rirUrl": {},
          "schema": "string",
          "sessionTimeout": "string",
          "settings": {
            "acceptedMimeTypes": [
              "string"
            ],
            "annotationListTable": {
              "columns": [
                {
                  "columnType": "string",
                  "metaName": "Ava Chen",
                  "visible": true,
                  "width": 1
                }
              ]
            },
            "columns": [
              {
                "schemaId": "string"
              }
            ],
            "dashboardCustomization": {
              "allDocuments": true,
              "confirmed": true,
              "deleted": true,
              "exported": true,
              "labels": true,
              "postponed": true,
              "rejected": true,
              "toReview": true
            },
            "emailNotifications": {
              "deletedAnnotations": true,
              "emailWithNoAttachments": true,
              "postponedAnnotations": true,
              "recipient": {},
              "unprocessableAttachments": true
            },
            "hideExportButton": true,
            "rejectionConfig": {
              "enabled": true
            },
            "suggestedEdit": "string",
            "suggestedRecipientsSources": [
              {
                "source": "string"
              }
            ],
            "uiOnEditConfirm": "string",
            "uiUploadEnabled": true,
            "uiValidationScreenEnabled": true,
            "workflows": {
              "bypassWorkflowsAllowed": true,
              "enabled": true
            }
          },
          "status": "string",
          "trainingEnabled": true,
          "url": "https://example.com",
          "useConfirmedState": true,
          "workspace": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.next` | object |  |
| `pagination.previous` | object |  |
| `results[].archiveEnabled` | boolean |  |
| `results[].automationEnabled` | boolean |  |
| `results[].automationLevel` | string |  |
| `results[].connector` | object |  |
| `results[].counts.confirmed` | number |  |
| `results[].counts.created` | number |  |
| `results[].counts.deleted` | number |  |
| `results[].counts.exported` | number |  |
| `results[].counts.exporting` | number |  |
| `results[].counts.failedExport` | number |  |
| `results[].counts.failedImport` | number |  |
| `results[].counts.importing` | number |  |
| `results[].counts.inWorkflow` | number |  |
| `results[].counts.postponed` | number |  |
| `results[].counts.purged` | number |  |
| `results[].counts.rejected` | number |  |
| `results[].counts.reviewing` | number |  |
| `results[].counts.split` | number |  |
| `results[].counts.toReview` | number |  |
| `results[].dedicatedEngine` | object |  |
| `results[].defaultScoreThreshold` | number |  |
| `results[].deleteAfter` | object |  |
| `results[].documentLifetime` | object |  |
| `results[].engine` | string |  |
| `results[].genericEngine` | object |  |
| `results[].id` | number |  |
| `results[].inbox` | string |  |
| `results[].locale` | string |  |
| `results[].metadata.queueTemplate` | string |  |
| `results[].modifiedAt` | string |  |
| `results[].modifiedBy` | object |  |
| `results[].name` | string |  |
| `results[].qualitySpotCheckPercentage` | number |  |
| `results[].rirParams` | object |  |
| `results[].rirUrl` | object |  |
| `results[].schema` | string |  |
| `results[].sessionTimeout` | string |  |
| `results[].settings.acceptedMimeTypes[]` | string |  |
| `results[].settings.annotationListTable.columns[].columnType` | string |  |
| `results[].settings.annotationListTable.columns[].metaName` | string |  |
| `results[].settings.annotationListTable.columns[].visible` | boolean |  |
| `results[].settings.annotationListTable.columns[].width` | number |  |
| `results[].settings.columns[].schemaId` | string |  |
| `results[].settings.dashboardCustomization.allDocuments` | boolean |  |
| `results[].settings.dashboardCustomization.confirmed` | boolean |  |
| `results[].settings.dashboardCustomization.deleted` | boolean |  |
| `results[].settings.dashboardCustomization.exported` | boolean |  |
| `results[].settings.dashboardCustomization.labels` | boolean |  |
| `results[].settings.dashboardCustomization.postponed` | boolean |  |
| `results[].settings.dashboardCustomization.rejected` | boolean |  |
| `results[].settings.dashboardCustomization.toReview` | boolean |  |
| `results[].settings.emailNotifications.deletedAnnotations` | boolean |  |
| `results[].settings.emailNotifications.emailWithNoAttachments` | boolean |  |
| `results[].settings.emailNotifications.postponedAnnotations` | boolean |  |
| `results[].settings.emailNotifications.recipient` | object |  |
| `results[].settings.emailNotifications.unprocessableAttachments` | boolean |  |
| `results[].settings.hideExportButton` | boolean |  |
| `results[].settings.rejectionConfig.enabled` | boolean |  |
| `results[].settings.suggestedEdit` | string |  |
| `results[].settings.suggestedRecipientsSources[].source` | string |  |
| `results[].settings.uiOnEditConfirm` | string |  |
| `results[].settings.uiUploadEnabled` | boolean |  |
| `results[].settings.uiValidationScreenEnabled` | boolean |  |
| `results[].settings.workflows.bypassWorkflowsAllowed` | boolean |  |
| `results[].settings.workflows.enabled` | boolean |  |
| `results[].status` | string |  |
| `results[].trainingEnabled` | boolean |  |
| `results[].url` | string |  |
| `results[].useConfirmedState` | boolean |  |
| `results[].workspace` | string |  |

## Native endpoint

Through the native Rossum API, this operation is `GET /queues` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-queues.md) for the provider-specific parameters and requirements.

