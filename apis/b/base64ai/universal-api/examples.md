# Base64.ai Universal API Examples

These examples use the MindCloud API key and Base64.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User

Retrieves user account details from Base64.ai.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/get-user?${params}`, {
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
      "ccEmails": [
        "ava@example.com"
      ],
      "companyName": "Ava Chen",
      "defaultFlowID": "string",
      "email": "ava@example.com",
      "familyName": "Ava Chen",
      "givenName": "Ava Chen",
      "hasActiveAwsContract": true,
      "hasSponsor": true,
      "isDomainAdmin": true,
      "isWorkEmailVerified": true,
      "numberOfCredits": 1,
      "numberOfCreditsSpentOnDocuments": 1,
      "numberOfPages": 1,
      "numberOfUploads": 1,
      "passkeys": [
        {}
      ],
      "phoneNumber": "string",
      "starred": {},
      "status": "string",
      "subscriptionPeriod": "string",
      "subscriptionType": "string",
      "tags": [
        "string"
      ],
      "tour": {
        "isDisabled": true,
        "welcomeCompleted": 1
      },
      "workEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get User action reference](actions/get-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/base64ai/latest/actions/get-user).

## Create Flow

Creates a new flow in Base64.ai.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/create-flow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/create-flow', {
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

Example response:

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
      "createdAt": "2026-05-07T12:00:00.000Z",
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
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Flow action reference](actions/create-flow.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/base64ai/latest/actions/create-flow).
