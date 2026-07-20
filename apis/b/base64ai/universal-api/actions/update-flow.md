# Base64.ai: Update Flow

Updates an existing flow in Base64.ai.

```
PUT https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/update-flow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Base64.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/update-flow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "flowId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/update-flow', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "flowId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `flowId` | string | yes | Flow identifier to update. |
| `name` | string | no | Updated flow name. |
| `status` | string | no | Updated flow status. Default: `enabled`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hitl` | object | no | Updated human-in-the-loop settings object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalListColumns": [
        {
          "displayName": "Ava Chen",
          "fieldName": "Ava Chen"
        }
      ],
      "administrators": [
        {}
      ],
      "allowedUploaders": [
        {}
      ],
      "allowPublicUploads": true,
      "createdBy": "string",
      "createdByDomain": "string",
      "createdByEmail": "ava@example.com",
      "dataRetention": {
        "status": "string"
      },
      "destination": {},
      "documentsToAsk": [
        {}
      ],
      "fileTypeDimensionLimits": [
        {}
      ],
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
      "name": "Ava Chen",
      "numberOfApproved": 1,
      "numberOfDeleted": 1,
      "numberOfError": 1,
      "numberOfNeedsReview": 1,
      "numberOfProcessing": 1,
      "numberOfRejected": 1,
      "numberOfUploads": 1,
      "onlyProcessLimitedMimeTypes": true,
      "postProcessing": {},
      "predefinedFields": [
        {}
      ],
      "questions": [
        {}
      ],
      "rejectionReasons": [
        {}
      ],
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
      "tableTaxonomies": [
        {}
      ],
      "tags": [
        "string"
      ],
      "taxonomies": [
        {}
      ],
      "updatedAt": {
        "Nanoseconds": 1,
        "Seconds": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalListColumns[].displayName` | string |  |
| `additionalListColumns[].fieldName` | string |  |
| `administrators[]` | object |  |
| `allowedUploaders[]` | object |  |
| `allowPublicUploads` | boolean |  |
| `createdBy` | string |  |
| `createdByDomain` | string |  |
| `createdByEmail` | string |  |
| `dataRetention.status` | string |  |
| `destination` | object |  |
| `documentsToAsk[]` | object |  |
| `fileTypeDimensionLimits[]` | object |  |
| `flowID` | string |  |
| `flowSearch.status` | string |  |
| `hideSampleFiles` | boolean |  |
| `hitl.allowReviewersToDownloadOriginalFiles` | boolean |  |
| `hitl.chartAggregateX` | boolean |  |
| `hitl.chartBackground` | string |  |
| `hitl.hideReviewerWatermarks` | boolean |  |
| `hitl.status` | string |  |
| `hitl.storeFiles` | boolean |  |
| `hitl.tableHighlightThreshold` | number |  |
| `hitl.tablePosition` | string |  |
| `id` | string |  |
| `instructions` | object |  |
| `isDefault` | boolean |  |
| `isOwner` | boolean |  |
| `name` | string |  |
| `numberOfApproved` | number |  |
| `numberOfDeleted` | number |  |
| `numberOfError` | number |  |
| `numberOfNeedsReview` | number |  |
| `numberOfProcessing` | number |  |
| `numberOfRejected` | number |  |
| `numberOfUploads` | number |  |
| `onlyProcessLimitedMimeTypes` | boolean |  |
| `postProcessing` | object |  |
| `predefinedFields[]` | object |  |
| `questions[]` | object |  |
| `rejectionReasons[]` | object |  |
| `resultManipulation.disableAllExceptMustHaveFields` | boolean |  |
| `reviewSla.status` | string |  |
| `roles[]` | string |  |
| `settings.allowIncompleteResults` | boolean |  |
| `settings.classificationFallback` | string |  |
| `settings.convertBlocksToFields` | boolean |  |
| `settings.convertTextToSpeech` | boolean |  |
| `settings.decodeVin` | boolean |  |
| `settings.defaultCurrency` | string |  |
| `settings.detectBarcodes` | boolean |  |
| `settings.detectBlur` | boolean |  |
| `settings.detectCheckboxes` | boolean |  |
| `settings.detectDatamatrix` | boolean |  |
| `settings.detectEnhancedIDs` | boolean |  |
| `settings.detectFaces` | boolean |  |
| `settings.detectFraud` | boolean |  |
| `settings.detectGlares` | boolean |  |
| `settings.detectIBAN` | boolean |  |
| `settings.detectQrCodes` | boolean |  |
| `settings.detectSignatures` | boolean |  |
| `settings.detectStamps` | boolean |  |
| `settings.detectWatermarks` | boolean |  |
| `settings.eagerProcessID` | boolean |  |
| `settings.extractExifData` | boolean |  |
| `settings.flattenTable` | boolean |  |
| `settings.generatePDF` | boolean |  |
| `settings.geocodeAddresses` | boolean |  |
| `settings.hideDom` | boolean |  |
| `settings.hideFieldLocations` | boolean |  |
| `settings.integrationConcurrency` | number |  |
| `settings.integrations.scanFromEmail.processAttachments` | boolean |  |
| `settings.integrations.scanFromEmail.processEmailMessage` | boolean |  |
| `settings.integrations.scanFromEmail.replyToSender` | boolean |  |
| `settings.keepOriginalTables` | boolean |  |
| `settings.mergeSemanticResults` | boolean |  |
| `settings.mergeTables` | boolean |  |
| `settings.processDocxOnly` | boolean |  |
| `settings.processExcelOnly` | boolean |  |
| `settings.readDigitalSignatures` | boolean |  |
| `settings.recognizeEntities` | boolean |  |
| `settings.renderLineItemsAsObjects` | boolean |  |
| `settings.runDocumentClassificationOnly` | boolean |  |
| `settings.usePretrainedModels` | boolean |  |
| `settings.useSegmentation` | boolean |  |
| `settings.verifyDocumentShape` | boolean |  |
| `status` | string |  |
| `suggestedQuestions[]` | string |  |
| `tableTaxonomies[]` | object |  |
| `tags[]` | string |  |
| `taxonomies[]` | object |  |
| `updatedAt.Nanoseconds` | number |  |
| `updatedAt.Seconds` | number |  |

## Native endpoint

Through the native Base64.ai API, this operation is `POST /api/flow/:flowId` (base URL `https://base64.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-flow.md) for the provider-specific parameters and requirements.

