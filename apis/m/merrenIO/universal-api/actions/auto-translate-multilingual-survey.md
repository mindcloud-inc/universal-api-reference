# MerrenIO: Auto Translate Multilingual Survey



```
PUT https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/auto-translate-multilingual-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MerrenIO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/auto-translate-multilingual-survey" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": "680000000000000000000000",
  "sourceLanguage": "English",
  "selectedLanguages": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/auto-translate-multilingual-survey', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": "680000000000000000000000",
    "sourceLanguage": "English",
    "selectedLanguages": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | string | yes | Survey to translate. Example: `680000000000000000000000`. |
| `sourceLanguage` | string | yes | Current language of the survey. Default: `English`. |
| `selectedLanguages` | string | yes | Languages Merren should translate the survey into. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MerrenIO API returns.

## Native endpoint

Through the native MerrenIO API, this operation is `POST /survey/checkAllowTranslation` (base URL `https://app.merren.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/auto-translate-multilingual-survey.md) for the provider-specific parameters and requirements.

