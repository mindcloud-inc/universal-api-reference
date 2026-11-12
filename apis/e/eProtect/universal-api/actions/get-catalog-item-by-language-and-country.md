# 3E Protect: Get Catalog Item by Language and Country



```
GET https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/get-catalog-item-by-language-and-country
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 3E Protect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/get-catalog-item-by-language-and-country?connectionId=$CONNECTION_ID&source=string&identifier=string&country=USA&locale=en" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "source": "string",
  "identifier": "string",
  "country": "USA",
  "locale": "en"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/get-catalog-item-by-language-and-country?${params}`, {
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
| `source` | string | yes | Exact, case-sensitive product identifier source name agreed with 3E. |
| `identifier` | string | yes | Your product identifier value for the selected source. |
| `country` | string | yes | Three-letter country code, such as USA. Use a country configured in List SDS Requirements. Example: `USA`. |
| `locale` | string | yes | Two-letter language code, such as en. Use a language configured in List SDS Requirements. Example: `en`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 3E Protect API returns.

## Native endpoint

Through the native 3E Protect API, this operation is `GET /catalog-item/:source/:identifier/:locale/:country` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-catalog-item-by-language-and-country.md) for the provider-specific parameters and requirements.

