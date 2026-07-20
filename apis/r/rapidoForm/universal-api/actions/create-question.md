# RapidoForm: Create Question

Creates a new question in RapidoForm.

```
POST https://connect.mindcloud.co/v1/universal/rapidoForm/latest/actions/create-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RapidoForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rapidoForm/latest/actions/create-question" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "questionDescription": "string",
  "questionOrder": 1,
  "questionText": "string",
  "surveyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rapidoForm/latest/actions/create-question', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "questionDescription": "string",
    "questionOrder": 1,
    "questionText": "string",
    "surveyId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `questionDescription` | string | yes |  |
| `questionOrder` | number | yes |  |
| `questionText` | string | yes |  |
| `questionType` | string | no |  |
| `surveyId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audioPlayerType": "string",
      "codingDifficultyMode": "string",
      "codingQuePoints": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "currencyType": "string",
      "focalPoint": {
        "x": 1,
        "y": 1
      },
      "hideBackBtn": true,
      "hideNextBtn": true,
      "Id": "string",
      "imagesCountPerRow": 1,
      "isBtnLink": true,
      "lowerBoundLevel": "string",
      "lowerBoundNumber": "string",
      "makeAudioOptional": true,
      "markOptional": true,
      "maxTextLength": 1,
      "mediaAltText": "string",
      "mediaBrightness": 1,
      "mediaMaxDuration": 1,
      "mediaPlayback": true,
      "minTextLength": 1,
      "nextBtnLink": "https://example.com",
      "optionRandomOrder": true,
      "paymentAccLabel": "string",
      "paymentAmt": 1,
      "payPalClientId": "string",
      "questionAnswer": "string",
      "questionOrder": 1,
      "questionText": "string",
      "questionType": "string",
      "randomGroupInd": 1,
      "randomizationAdd": true,
      "ratingScale": 1,
      "ratingSliderOn": true,
      "ratingType": "string",
      "rule": "string",
      "selectionType": "string",
      "setMaxTextLength": true,
      "setMediaMaxDuration": true,
      "setMinTextLength": true,
      "setTimeMinimum": true,
      "shuffleImages": true,
      "silenceCheck": true,
      "sliderIncrement": 1,
      "statementQueBtnText": "string",
      "stimuliMedia": {
        "iconColor": "string",
        "layoutType": "string",
        "mediaFormat": "string",
        "mediaLink": "https://example.com",
        "mobileLayoutType": "string"
      },
      "stripeAccId": "string",
      "surveyId": "string",
      "timeMinimum": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uploadLimit": 1,
      "upperBoundLevel": "string",
      "upperBoundNumber": 1,
      "V": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audioPlayerType` | string |  |
| `codingDifficultyMode` | string |  |
| `codingQuePoints` | number |  |
| `createdAt` | date |  |
| `creatorId` | string |  |
| `currencyType` | string |  |
| `focalPoint.x` | number |  |
| `focalPoint.y` | number |  |
| `hideBackBtn` | boolean |  |
| `hideNextBtn` | boolean |  |
| `Id` | string |  |
| `imagesCountPerRow` | number |  |
| `isBtnLink` | boolean |  |
| `lowerBoundLevel` | string |  |
| `lowerBoundNumber` | string |  |
| `makeAudioOptional` | boolean |  |
| `markOptional` | boolean |  |
| `maxTextLength` | number |  |
| `mediaAltText` | string |  |
| `mediaBrightness` | number |  |
| `mediaMaxDuration` | number |  |
| `mediaPlayback` | boolean |  |
| `minTextLength` | number |  |
| `nextBtnLink` | string |  |
| `optionRandomOrder` | boolean |  |
| `paymentAccLabel` | string |  |
| `paymentAmt` | number |  |
| `payPalClientId` | string |  |
| `questionAnswer` | string |  |
| `questionOrder` | number |  |
| `questionText` | string |  |
| `questionType` | string |  |
| `randomGroupInd` | number |  |
| `randomizationAdd` | boolean |  |
| `ratingScale` | number |  |
| `ratingSliderOn` | boolean |  |
| `ratingType` | string |  |
| `rule` | string |  |
| `selectionType` | string |  |
| `setMaxTextLength` | boolean |  |
| `setMediaMaxDuration` | boolean |  |
| `setMinTextLength` | boolean |  |
| `setTimeMinimum` | boolean |  |
| `shuffleImages` | boolean |  |
| `silenceCheck` | boolean |  |
| `sliderIncrement` | number |  |
| `statementQueBtnText` | string |  |
| `stimuliMedia.iconColor` | string |  |
| `stimuliMedia.layoutType` | string |  |
| `stimuliMedia.mediaFormat` | string |  |
| `stimuliMedia.mediaLink` | string |  |
| `stimuliMedia.mobileLayoutType` | string |  |
| `stripeAccId` | string |  |
| `surveyId` | string |  |
| `timeMinimum` | number |  |
| `updatedAt` | date |  |
| `uploadLimit` | number |  |
| `upperBoundLevel` | string |  |
| `upperBoundNumber` | number |  |
| `V` | number |  |

## Native endpoint

Through the native RapidoForm API, this operation is `POST /api/question` (base URL `https://www.rapidoform.com/be`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-question.md) for the provider-specific parameters and requirements.

