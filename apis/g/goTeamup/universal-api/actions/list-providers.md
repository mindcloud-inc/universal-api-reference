# GoTeamup: List Providers

Finds providers in GoTeamup.

```
GET https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-providers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-providers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-providers?${params}`, {
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
      "country": "string",
      "currency": {
        "isoCurrencyCode": "string",
        "position": "string",
        "symbol": "string"
      },
      "description": "string",
      "id": 1,
      "isMarketingPreferenceOnCustomerForms": true,
      "logo": {
        "originalHeight": {},
        "originalWidth": {},
        "url": "https://example.com"
      },
      "name": "Ava Chen",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `currency.isoCurrencyCode` | string |  |
| `currency.position` | string |  |
| `currency.symbol` | string |  |
| `description` | string |  |
| `id` | number |  |
| `isMarketingPreferenceOnCustomerForms` | boolean |  |
| `logo.originalHeight` | object |  |
| `logo.originalWidth` | object |  |
| `logo.url` | string |  |
| `name` | string |  |
| `object` | string |  |

## Native endpoint

Through the native GoTeamup API, this operation is `GET /providers` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-providers.md) for the provider-specific parameters and requirements.

