# Transifex: Get Translation Download



```
GET https://connect.mindcloud.co/v1/universal/transifex/latest/actions/get-translation-download
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transifex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transifex/latest/actions/get-translation-download?connectionId=$CONNECTION_ID&resourceTranslationsAsyncDownloadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceTranslationsAsyncDownloadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transifex/latest/actions/get-translation-download?${params}`, {
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
| `resourceTranslationsAsyncDownloadId` | string | yes | The Transifex async translation download identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "string10": "string",
      "string11": "string",
      "string12": "string",
      "string13": "string",
      "string14": "string",
      "string15": "string",
      "string16": "string",
      "string17": "string",
      "string18": "string",
      "string2": "string",
      "string3": "string",
      "string4": "string",
      "string5": "string",
      "string6": "string",
      "string7": "string",
      "string8": "string",
      "string9": "string",
      "welcome_string": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `string10` | string |  |
| `string11` | string |  |
| `string12` | string |  |
| `string13` | string |  |
| `string14` | string |  |
| `string15` | string |  |
| `string16` | string |  |
| `string17` | string |  |
| `string18` | string |  |
| `string2` | string |  |
| `string3` | string |  |
| `string4` | string |  |
| `string5` | string |  |
| `string6` | string |  |
| `string7` | string |  |
| `string8` | string |  |
| `string9` | string |  |
| `welcome_string` | string |  |

## Native endpoint

Through the native Transifex API, this operation is `GET /resource_translations_async_downloads/:resource_translations_async_download_id` (base URL `https://rest.api.transifex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-translation-download.md) for the provider-specific parameters and requirements.

