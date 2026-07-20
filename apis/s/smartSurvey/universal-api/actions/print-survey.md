# SmartSurvey: Print Survey

Renders a SmartSurvey survey as HTML, Word, or PDF.

```
GET https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/print-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/print-survey?connectionId=$CONNECTION_ID&surveyId=1&t=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "1",
  "t": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/print-survey?${params}`, {
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
| `surveyId` | number | yes | The survey id of the survey you want to print |
| `t` | number | yes | The output type you want to print the survey as. Options: 1: Word doc \| 2: HTML \| 3: PDF |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `st` | number | no | The survey translation id to print the survey in. |
| `dst` | boolean | no | Whether to include the title of the survey. (default: true) |
| `dsl` | boolean | no | Whether to include the logo. (default: true) |
| `qn` | boolean | no | Whether to include question numbers. (default: true) |
| `pn` | boolean | no | Whether to include page numbers. (default: true) |
| `pt` | boolean | no | Whether to include page headings. (default: true) |
| `pd` | boolean | no | Whether to include page descriptions. (default: true) |
| `pb` | boolean | no | Whether to include page breaks. (default: true) |
| `pqb` | boolean | no | Whether to prevent breaking questions across pages. (default: true) |
| `qf` | boolean | no | Whether to strip HTML tags from all questions. (default: false) |
| `of` | boolean | no | Whether to strip HTML tags from all answer choices. (default: false) |
| `stbg` | string | no | The background color of the survey title. (default: #1170a8 - dark blue) |
| `stc` | string | no | The color of the survey title text. (default: #FFFFFF - white) |
| `slbg` | string | no | The background color of the survey logo. (default: #FFFFFF - white) |
| `ptbg` | string | no | The background color of the page title. (default: #424242 - dark gray/black) |
| `ptc` | string | no | The color of the page title text. (default: #FFFFFF - white) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native SmartSurvey API, this operation is `GET /surveys/{surveyId}/print` (base URL `https://api.smartsurvey.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/print-survey.md) for the provider-specific parameters and requirements.

