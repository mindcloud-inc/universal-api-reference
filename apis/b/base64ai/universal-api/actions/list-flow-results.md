# Base64.ai: List Flow Results

Retrieves results from a specific Base64.ai flow.

```
GET https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/list-flow-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Base64.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/list-flow-results?connectionId=$CONNECTION_ID&flowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "flowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/list-flow-results?${params}`, {
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
| `flowId` | string | yes | Flow identifier whose results should be listed. |
| `limit` | number | no | Maximum number of results to return. Default: `25`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "flow": {
        "additionalListColumns": [
          {
            "displayName": "Ava Chen",
            "fieldName": "Ava Chen"
          }
        ],
        "allowPublicUploads": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "createdBy": "string",
        "createdByDomain": "string",
        "createdByEmail": "ava@example.com",
        "dataRetention": {
          "status": "string"
        },
        "flowID": "string",
        "flowSearch": {
          "status": "string"
        },
        "hideSampleFiles": true,
        "hitl": {
          "allowReviewersToDownloadOriginalFiles": true,
          "chartAggregateX": true,
          "chartBackground": "string",
          "hideReviewerWatermarks": true,
          "status": "string",
          "storeFiles": true,
          "tableHighlightThreshold": 1,
          "tablePosition": "string"
        },
        "id": "string",
        "instructions": {},
        "isDefault": true,
        "isOwner": true,
        "lastUploadedAt": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "numberOfApproved": 1,
        "numberOfDeleted": 1,
        "numberOfError": 1,
        "numberOfNeedsReview": 1,
        "numberOfProcessing": 1,
        "numberOfRejected": 1,
        "numberOfUploads": 1,
        "onlyProcessLimitedMimeTypes": true,
        "resultManipulation": {
          "disableAllExceptMustHaveFields": true
        },
        "reviewSla": {
          "status": "string"
        },
        "roles": [
          "string"
        ],
        "settings": {
          "allowIncompleteResults": true,
          "classificationFallback": "string",
          "convertBlocksToFields": true,
          "convertTextToSpeech": true,
          "decodeVin": true,
          "defaultCurrency": "string",
          "detectBarcodes": true,
          "detectBlur": true,
          "detectCheckboxes": true,
          "detectDatamatrix": true,
          "detectEnhancedIDs": true,
          "detectFaces": true,
          "detectFraud": true,
          "detectGlares": true,
          "detectIBAN": true,
          "detectQrCodes": true,
          "detectSignatures": true,
          "detectStamps": true,
          "detectWatermarks": true,
          "eagerProcessID": true,
          "extractExifData": true,
          "flattenTable": true,
          "generatePDF": true,
          "geocodeAddresses": true,
          "hideDom": true,
          "hideFieldLocations": true,
          "integrationConcurrency": 1,
          "integrations": {
            "scanFromEmail": {
              "processAttachments": true,
              "processEmailMessage": true,
              "replyToSender": true
            }
          },
          "keepOriginalTables": true,
          "mergeSemanticResults": true,
          "mergeTables": true,
          "processDocxOnly": true,
          "processExcelOnly": true,
          "readDigitalSignatures": true,
          "recognizeEntities": true,
          "renderLineItemsAsObjects": true,
          "runDocumentClassificationOnly": true,
          "usePretrainedModels": true,
          "useSegmentation": true,
          "verifyDocumentShape": true
        },
        "status": "string",
        "suggestedQuestions": [
          "string"
        ],
        "tags": [
          "string"
        ],
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "orderBy": "string",
      "results": [
        {
          "additionalListColumns": {
            "*modelName": "Ava Chen",
            "*updatedAt": 1
          },
          "createdAt": "2026-05-07T12:00:00.000Z",
          "createdBy": "string",
          "fileName": "Ava Chen",
          "isFirst": true,
          "isLast": true,
          "linkedResults": [
            "https://example.com"
          ],
          "model": {
            "name": "Ava Chen",
            "type": "string"
          },
          "resultUuid": "string",
          "startPage": 1,
          "status": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "uploadedBy": "string"
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
| `flow.additionalListColumns[].displayName` | string |  |
| `flow.additionalListColumns[].fieldName` | string |  |
| `flow.allowPublicUploads` | boolean |  |
| `flow.createdAt` | date |  |
| `flow.createdBy` | string |  |
| `flow.createdByDomain` | string |  |
| `flow.createdByEmail` | string |  |
| `flow.dataRetention.status` | string |  |
| `flow.flowID` | string |  |
| `flow.flowSearch.status` | string |  |
| `flow.hideSampleFiles` | boolean |  |
| `flow.hitl.allowReviewersToDownloadOriginalFiles` | boolean |  |
| `flow.hitl.chartAggregateX` | boolean |  |
| `flow.hitl.chartBackground` | string |  |
| `flow.hitl.hideReviewerWatermarks` | boolean |  |
| `flow.hitl.status` | string |  |
| `flow.hitl.storeFiles` | boolean |  |
| `flow.hitl.tableHighlightThreshold` | number |  |
| `flow.hitl.tablePosition` | string |  |
| `flow.id` | string |  |
| `flow.instructions` | object |  |
| `flow.isDefault` | boolean |  |
| `flow.isOwner` | boolean |  |
| `flow.lastUploadedAt` | date |  |
| `flow.name` | string |  |
| `flow.numberOfApproved` | number |  |
| `flow.numberOfDeleted` | number |  |
| `flow.numberOfError` | number |  |
| `flow.numberOfNeedsReview` | number |  |
| `flow.numberOfProcessing` | number |  |
| `flow.numberOfRejected` | number |  |
| `flow.numberOfUploads` | number |  |
| `flow.onlyProcessLimitedMimeTypes` | boolean |  |
| `flow.resultManipulation.disableAllExceptMustHaveFields` | boolean |  |
| `flow.reviewSla.status` | string |  |
| `flow.roles[]` | string |  |
| `flow.settings.allowIncompleteResults` | boolean |  |
| `flow.settings.classificationFallback` | string |  |
| `flow.settings.convertBlocksToFields` | boolean |  |
| `flow.settings.convertTextToSpeech` | boolean |  |
| `flow.settings.decodeVin` | boolean |  |
| `flow.settings.defaultCurrency` | string |  |
| `flow.settings.detectBarcodes` | boolean |  |
| `flow.settings.detectBlur` | boolean |  |
| `flow.settings.detectCheckboxes` | boolean |  |
| `flow.settings.detectDatamatrix` | boolean |  |
| `flow.settings.detectEnhancedIDs` | boolean |  |
| `flow.settings.detectFaces` | boolean |  |
| `flow.settings.detectFraud` | boolean |  |
| `flow.settings.detectGlares` | boolean |  |
| `flow.settings.detectIBAN` | boolean |  |
| `flow.settings.detectQrCodes` | boolean |  |
| `flow.settings.detectSignatures` | boolean |  |
| `flow.settings.detectStamps` | boolean |  |
| `flow.settings.detectWatermarks` | boolean |  |
| `flow.settings.eagerProcessID` | boolean |  |
| `flow.settings.extractExifData` | boolean |  |
| `flow.settings.flattenTable` | boolean |  |
| `flow.settings.generatePDF` | boolean |  |
| `flow.settings.geocodeAddresses` | boolean |  |
| `flow.settings.hideDom` | boolean |  |
| `flow.settings.hideFieldLocations` | boolean |  |
| `flow.settings.integrationConcurrency` | number |  |
| `flow.settings.integrations.scanFromEmail.processAttachments` | boolean |  |
| `flow.settings.integrations.scanFromEmail.processEmailMessage` | boolean |  |
| `flow.settings.integrations.scanFromEmail.replyToSender` | boolean |  |
| `flow.settings.keepOriginalTables` | boolean |  |
| `flow.settings.mergeSemanticResults` | boolean |  |
| `flow.settings.mergeTables` | boolean |  |
| `flow.settings.processDocxOnly` | boolean |  |
| `flow.settings.processExcelOnly` | boolean |  |
| `flow.settings.readDigitalSignatures` | boolean |  |
| `flow.settings.recognizeEntities` | boolean |  |
| `flow.settings.renderLineItemsAsObjects` | boolean |  |
| `flow.settings.runDocumentClassificationOnly` | boolean |  |
| `flow.settings.usePretrainedModels` | boolean |  |
| `flow.settings.useSegmentation` | boolean |  |
| `flow.settings.verifyDocumentShape` | boolean |  |
| `flow.status` | string |  |
| `flow.suggestedQuestions[]` | string |  |
| `flow.tags[]` | string |  |
| `flow.updatedAt` | date |  |
| `orderBy` | string |  |
| `results[].additionalListColumns.*modelName` | string |  |
| `results[].additionalListColumns.*updatedAt` | number |  |
| `results[].createdAt` | date |  |
| `results[].createdBy` | string |  |
| `results[].fileName` | string |  |
| `results[].isFirst` | boolean |  |
| `results[].isLast` | boolean |  |
| `results[].linkedResults[]` | string |  |
| `results[].model.name` | string |  |
| `results[].model.type` | string |  |
| `results[].resultUuid` | string |  |
| `results[].startPage` | number |  |
| `results[].status` | string |  |
| `results[].updatedAt` | date |  |
| `results[].uploadedBy` | string |  |

## Native endpoint

Through the native Base64.ai API, this operation is `GET /api/result` (base URL `https://base64.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-flow-results.md) for the provider-specific parameters and requirements.

