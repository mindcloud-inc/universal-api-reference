# Bluebarry: Get Question

Retrieves a single question from Bluebarry.

```
GET https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/get-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluebarry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/get-question?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/get-question?${params}`, {
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
| `id` | string | yes |  |

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

Through the native Bluebarry API, this operation is `GET /data/Questions({id})` (base URL `https://data.bluebarry.ai/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-question.md) for the provider-specific parameters and requirements.

