# serviceminder.io: List Features

Retrieves available features from ServiceMinder.

```
GET https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/list-features
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a serviceminder.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/list-features?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/list-features?${params}`, {
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
      "channels": [
        {}
      ],
      "cities": [
        {}
      ],
      "features": [
        "string"
      ],
      "leadSourceCategories": [
        {}
      ],
      "message": "string",
      "namedTaxRates": [
        {}
      ],
      "postalCodes": [
        "string"
      ],
      "resultCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels` | array<object> |  |
| `cities` | array<object> |  |
| `features` | array<string> |  |
| `leadSourceCategories` | array<object> |  |
| `message` | string |  |
| `namedTaxRates` | array<object> |  |
| `postalCodes` | array<string> |  |
| `resultCode` | number |  |

## Native endpoint

Through the native serviceminder.io API, this operation is `POST /settings/features` (base URL `https://serviceminder.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-features.md) for the provider-specific parameters and requirements.

