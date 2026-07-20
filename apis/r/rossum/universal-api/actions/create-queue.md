# Rossum: Create Queue

Creates a new queue in Rossum.

```
POST https://connect.mindcloud.co/v1/universal/rossum/latest/actions/create-queue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/create-queue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "workspace": "string",
  "schema": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rossum/latest/actions/create-queue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "workspace": "string",
    "schema": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the queue to create. |
| `workspace` | string | yes | Workspace URL where the queue should be created. |
| `schema` | string | yes | Schema URL applied to annotations in the queue. |

## Response

```json
{
  "success": true,
  "data": [
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
      "engine": {},
      "genericEngine": "string",
      "id": 1,
      "inbox": {},
      "locale": "string",
      "modifiedAt": "string",
      "modifiedBy": "string",
      "name": "Ava Chen",
      "qualitySpotCheckPercentage": 1,
      "rirParams": {},
      "rirUrl": {},
      "schema": "string",
      "sessionTimeout": "string",
      "settings": {
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archiveEnabled` | boolean |  |
| `automationEnabled` | boolean |  |
| `automationLevel` | string |  |
| `connector` | object |  |
| `counts.confirmed` | number |  |
| `counts.created` | number |  |
| `counts.deleted` | number |  |
| `counts.exported` | number |  |
| `counts.exporting` | number |  |
| `counts.failedExport` | number |  |
| `counts.failedImport` | number |  |
| `counts.importing` | number |  |
| `counts.inWorkflow` | number |  |
| `counts.postponed` | number |  |
| `counts.purged` | number |  |
| `counts.rejected` | number |  |
| `counts.reviewing` | number |  |
| `counts.split` | number |  |
| `counts.toReview` | number |  |
| `dedicatedEngine` | object |  |
| `defaultScoreThreshold` | number |  |
| `deleteAfter` | object |  |
| `documentLifetime` | object |  |
| `engine` | object |  |
| `genericEngine` | string |  |
| `id` | number |  |
| `inbox` | object |  |
| `locale` | string |  |
| `modifiedAt` | string |  |
| `modifiedBy` | string |  |
| `name` | string |  |
| `qualitySpotCheckPercentage` | number |  |
| `rirParams` | object |  |
| `rirUrl` | object |  |
| `schema` | string |  |
| `sessionTimeout` | string |  |
| `settings.dashboardCustomization.allDocuments` | boolean |  |
| `settings.dashboardCustomization.confirmed` | boolean |  |
| `settings.dashboardCustomization.deleted` | boolean |  |
| `settings.dashboardCustomization.exported` | boolean |  |
| `settings.dashboardCustomization.labels` | boolean |  |
| `settings.dashboardCustomization.postponed` | boolean |  |
| `settings.dashboardCustomization.rejected` | boolean |  |
| `settings.dashboardCustomization.toReview` | boolean |  |
| `settings.emailNotifications.deletedAnnotations` | boolean |  |
| `settings.emailNotifications.emailWithNoAttachments` | boolean |  |
| `settings.emailNotifications.postponedAnnotations` | boolean |  |
| `settings.emailNotifications.recipient` | object |  |
| `settings.emailNotifications.unprocessableAttachments` | boolean |  |
| `settings.rejectionConfig.enabled` | boolean |  |
| `settings.suggestedEdit` | string |  |
| `settings.suggestedRecipientsSources[].source` | string |  |
| `settings.uiOnEditConfirm` | string |  |
| `settings.uiUploadEnabled` | boolean |  |
| `settings.uiValidationScreenEnabled` | boolean |  |
| `settings.workflows.bypassWorkflowsAllowed` | boolean |  |
| `settings.workflows.enabled` | boolean |  |
| `status` | string |  |
| `trainingEnabled` | boolean |  |
| `url` | string |  |
| `useConfirmedState` | boolean |  |
| `workspace` | string |  |

## Native endpoint

Through the native Rossum API, this operation is `POST /queues` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-queue.md) for the provider-specific parameters and requirements.

