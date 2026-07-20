# AccuWeather: List Supported Languages

Lists the supported languages in AccuWeather.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-supported-languages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-supported-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-supported-languages?${params}`, {
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
      "DisplayName": "Ava Chen",
      "ID": 1,
      "ISO": "string",
      "LanguageType": 1,
      "LocalizedName": "Ava Chen",
      "MicroSoftCode": "string",
      "MicroSoftName": "Ava Chen",
      "Name": "Ava Chen",
      "TimeStamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `DisplayName` | string | Display name for the language. |
| `ID` | number | Numeric AccuWeather language identifier. |
| `ISO` | string | AccuWeather language code. |
| `LanguageType` | number | AccuWeather language type identifier. |
| `LocalizedName` | string | Localized display name. |
| `MicroSoftCode` | string | Microsoft language code. |
| `MicroSoftName` | string | Microsoft language display name. |
| `Name` | string | Canonical language name token. |
| `TimeStamp` | string | Timestamp for the language definition. |

## Native endpoint

Through the native AccuWeather API, this operation is `GET /translations/v1/languages` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-supported-languages.md) for the provider-specific parameters and requirements.

