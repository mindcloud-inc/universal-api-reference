# Monta: Detect Location

Detects a user's location by IP address in Monta.

```
GET https://connect.mindcloud.co/v1/universal/monta/latest/actions/detect-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monta/latest/actions/detect-location?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monta/latest/actions/detect-location?${params}`, {
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
      "availableCountries": [
        {
          "code": "string",
          "currencyCode": "string",
          "currencyName": "Ava Chen",
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "detectedCountry": {
        "code": "string",
        "currencyCode": "string",
        "currencyName": "Ava Chen",
        "id": 1,
        "isSanctioned": true,
        "name": "Ava Chen"
      },
      "detectedLanguage": "string",
      "isReliable": true,
      "warningMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableCountries[].code` | string |  |
| `availableCountries[].currencyCode` | string |  |
| `availableCountries[].currencyName` | string |  |
| `availableCountries[].id` | number |  |
| `availableCountries[].name` | string |  |
| `detectedCountry.code` | string |  |
| `detectedCountry.currencyCode` | string |  |
| `detectedCountry.currencyName` | string |  |
| `detectedCountry.id` | number |  |
| `detectedCountry.isSanctioned` | boolean |  |
| `detectedCountry.name` | string |  |
| `detectedLanguage` | string |  |
| `isReliable` | boolean |  |
| `warningMessage` | string |  |

## Native endpoint

Through the native Monta API, this operation is `GET /signup/detect-location` (base URL `https://public-api.monta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-location.md) for the provider-specific parameters and requirements.

