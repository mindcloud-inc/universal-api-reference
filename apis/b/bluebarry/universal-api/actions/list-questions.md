# Bluebarry: List Questions

Retrieves question entity records from Bluebarry.

```
GET https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/list-questions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluebarry `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/list-questions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/list-questions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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

Through the native Bluebarry API, this operation is `GET /data/Questions` (base URL `https://data.bluebarry.ai/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-questions.md) for the provider-specific parameters and requirements.

