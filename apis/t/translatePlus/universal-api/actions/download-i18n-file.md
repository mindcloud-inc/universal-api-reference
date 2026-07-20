# TranslatePlus: Download I18n File

Downloads a translated i18n file from TranslatePlus.

```
GET https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/download-i18n-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TranslatePlus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/download-i18n-file?connectionId=$CONNECTION_ID&jobId=string&languageCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string",
  "languageCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/download-i18n-file?${params}`, {
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
| `jobId` | string | yes | The i18n translation job UUID. |
| `languageCode` | string | yes | Target language code to download, such as fr. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file` | string |  |

## Native endpoint

Through the native TranslatePlus API, this operation is `GET /v2/translate/i18n/jobs/{job_id}/download` (base URL `https://api.translateplus.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-i18n-file.md) for the provider-specific parameters and requirements.

