# MerrenIO: Manually Edit Translations



```
PUT https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/manually-edit-translations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MerrenIO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/manually-edit-translations" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": "680000000000000000000000",
  "questionId": "690000000000000000000000",
  "languageType": "Spanish",
  "translatedText": "Texto traducido"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/manually-edit-translations', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": "680000000000000000000000",
    "questionId": "690000000000000000000000",
    "languageType": "Spanish",
    "translatedText": "Texto traducido"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | string | yes | Survey containing the translation to edit. Example: `680000000000000000000000`. |
| `questionId` | string | yes | Question whose translation should be updated. Example: `690000000000000000000000`. |
| `languageType` | string | yes | Language to edit. Default: `Spanish`. |
| `translatedText` | string | yes | Replacement translation text. Example: `Texto traducido`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MerrenIO API returns.

## Native endpoint

Through the native MerrenIO API, this operation is `POST /question/updateTranslationQustion` (base URL `https://app.merren.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/manually-edit-translations.md) for the provider-specific parameters and requirements.

