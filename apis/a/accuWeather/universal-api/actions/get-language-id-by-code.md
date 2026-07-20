# AccuWeather: Get Language Id By Code

Retrieves a language ID from AccuWeather by code.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-language-id-by-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-language-id-by-code?connectionId=$CONNECTION_ID&languageCode=en-us" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "languageCode": "en-us"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-language-id-by-code?${params}`, {
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
| `languageCode` | string | yes | Required AccuWeather language code. Default: `en-us`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | number | Language ID value. |

## Native endpoint

Through the native AccuWeather API, this operation is `GET /translations/v1/languages/code/:languageCode` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-language-id-by-code.md) for the provider-specific parameters and requirements.

