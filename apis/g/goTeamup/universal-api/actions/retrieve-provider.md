# GoTeamup: Retrieve Provider

Retrieves a provider from GoTeamup.

```
GET https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/retrieve-provider
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/retrieve-provider?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/retrieve-provider?${params}`, {
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
| `id` | number | yes | The TeamUp provider ID. |

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

Through the native GoTeamup API, this operation is `GET /providers/:id` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-provider.md) for the provider-specific parameters and requirements.

