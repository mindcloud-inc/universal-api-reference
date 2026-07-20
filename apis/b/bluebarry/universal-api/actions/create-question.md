# Bluebarry: Create Question

Creates a new question in Bluebarry.

```
POST https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/create-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluebarry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/create-question" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/create-question', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "advisorId": "string",
      "answers": [
        {}
      ],
      "autoApplyDiscountCode": true,
      "clonedFrom": "string",
      "consentText": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "desktopLayout": "string",
      "discountCode": "string",
      "displayType": "string",
      "extraInformation": "string",
      "filterRanking": "string",
      "fullQuestionText": "string",
      "id": "string",
      "imageFocalPointX": "string",
      "imageFocalPointY": "string",
      "imageUrl": "https://example.com",
      "interstitialSettings": "string",
      "interstitialTemplate": "string",
      "mobileLayout": "string",
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "modifierId": "string",
      "multipleSelectionBehavior": "string",
      "order": 1,
      "pictureAnswerLayout": "string",
      "questionTexts": [
        {}
      ],
      "reference": "string",
      "requireConsent": true,
      "required": true,
      "showDescription": true,
      "showImage": true,
      "showSkipOption": true,
      "skipButtonText": "string",
      "staticName": "Ava Chen",
      "tenant": "string",
      "tenantId": "string",
      "type": "string",
      "useAnswerGrid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `advisorId` | string |  |
| `answers` | array<object> |  |
| `autoApplyDiscountCode` | boolean |  |
| `clonedFrom` | string |  |
| `consentText` | string |  |
| `createdDate` | date |  |
| `creatorId` | string |  |
| `desktopLayout` | string |  |
| `discountCode` | string |  |
| `displayType` | string |  |
| `extraInformation` | string |  |
| `filterRanking` | string |  |
| `fullQuestionText` | string |  |
| `id` | string |  |
| `imageFocalPointX` | string |  |
| `imageFocalPointY` | string |  |
| `imageUrl` | string |  |
| `interstitialSettings` | string |  |
| `interstitialTemplate` | string |  |
| `mobileLayout` | string |  |
| `modifiedDate` | date |  |
| `modifierId` | string |  |
| `multipleSelectionBehavior` | string |  |
| `order` | number |  |
| `pictureAnswerLayout` | string |  |
| `questionTexts` | array<object> |  |
| `reference` | string |  |
| `requireConsent` | boolean |  |
| `required` | boolean |  |
| `showDescription` | boolean |  |
| `showImage` | boolean |  |
| `showSkipOption` | boolean |  |
| `skipButtonText` | string |  |
| `staticName` | string |  |
| `tenant` | string |  |
| `tenantId` | string |  |
| `type` | string |  |
| `useAnswerGrid` | boolean |  |

## Native endpoint

Through the native Bluebarry API, this operation is `POST /data/Questions` (base URL `https://data.bluebarry.ai/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-question.md) for the provider-specific parameters and requirements.

