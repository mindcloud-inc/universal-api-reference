# Appwrite: Get user locale

Retrieves the user locale from Appwrite.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/locale-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/locale-get?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/locale-get?${params}`, {
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
      "continent": "string",
      "continentCode": "string",
      "country": "string",
      "countryCode": "string",
      "currency": "string",
      "eu": true,
      "ip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `continent` | string | Continent name. This field support localization. |
| `continentCode` | string | Continent code. A two character continent code "AF" for Africa, "AN" for Antarctica, "AS" for Asia, "EU" for Europe, "NA" for North America, "OC" for Oceania, and "SA" for South America. |
| `country` | string | Country name. This field support localization. |
| `countryCode` | string | Country code in [ISO 3166-1](http://en.wikipedia.org/wiki/ISO_3166-1) two-character format |
| `currency` | string | Currency code in [ISO 4217-1](http://en.wikipedia.org/wiki/ISO_4217) three-character format |
| `eu` | boolean | True if country is part of the European Union. |
| `ip` | string | User IP address. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /locale` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/locale-get.md) for the provider-specific parameters and requirements.

