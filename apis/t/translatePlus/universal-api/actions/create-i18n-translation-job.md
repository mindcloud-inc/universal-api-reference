# TranslatePlus: Create I18n Translation Job

Creates a new i18n translation job in TranslatePlus.

```
POST https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/create-i18n-translation-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TranslatePlus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/create-i18n-translation-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "targetLanguages": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/create-i18n-translation-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "targetLanguages": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Upload a JSON, YAML, CSV, Properties, or XML localization file. |
| `sourceLanguage` | string | no | Default: `auto`. |
| `targetLanguages` | string | yes | Comma-separated target language codes such as fr,de. |
| `webhookUrl` | string | no | Optional URL that receives job-completion callbacks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job_id": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job_id` | string |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TranslatePlus API, this operation is `POST /v2/translate/i18n` (base URL `https://api.translateplus.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-i18n-translation-job.md) for the provider-specific parameters and requirements.

