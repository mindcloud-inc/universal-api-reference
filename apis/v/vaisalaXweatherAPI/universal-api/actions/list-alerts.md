# Vaisala Xweather: List Alerts

Retrieves alerts from Vaisala Xweather API.

```
GET https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/list-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vaisala Xweather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/list-alerts?connectionId=$CONNECTION_ID&id=seattle%2Cwa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "seattle,wa"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/list-alerts?${params}`, {
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
| `id` | string | yes | Location, place identifier, or latitude/longitude. Example: `seattle,wa`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "dataSource": "string",
      "details": {},
      "id": "string",
      "includes": {},
      "loc": {},
      "localLanguages": [
        {}
      ],
      "place": {},
      "poly": "string",
      "profile": {},
      "timestamps": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `dataSource` | string |  |
| `details` | object |  |
| `id` | string |  |
| `includes` | object |  |
| `loc` | object |  |
| `localLanguages` | array<object> |  |
| `place` | object |  |
| `poly` | string |  |
| `profile` | object |  |
| `timestamps` | object |  |

## Native endpoint

Through the native Vaisala Xweather API, this operation is `GET /alerts/:id` (base URL `https://data.api.xweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-alerts.md) for the provider-specific parameters and requirements.

