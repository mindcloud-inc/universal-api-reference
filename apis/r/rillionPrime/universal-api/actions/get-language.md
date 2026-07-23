# Rillion Prime: Get Language



```
GET https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/get-language
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/get-language?connectionId=$CONNECTION_ID&languageID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "languageID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/get-language?${params}`, {
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
| `languageID` | string | yes | Path value for LanguageID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateFormat": "string",
      "dateSeparator": "string",
      "decimalSymbol": "string",
      "digitGroupingSymbol": "string",
      "language": "string",
      "languageID": "string",
      "timeFormat": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateFormat` | string |  |
| `dateSeparator` | string |  |
| `decimalSymbol` | string |  |
| `digitGroupingSymbol` | string |  |
| `language` | string |  |
| `languageID` | string |  |
| `timeFormat` | string |  |

## Native endpoint

Through the native Rillion Prime API, this operation is `GET /language/:LanguageID` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-language.md) for the provider-specific parameters and requirements.

