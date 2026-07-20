# Brasil API: Get City Weather Forecast

Retrieves a one-day city weather forecast from Brasil API.

```
GET https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-city-weather-forecast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brasil API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-city-weather-forecast?connectionId=$CONNECTION_ID&cityCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cityCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-city-weather-forecast?${params}`, {
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
| `cityCode` | string | yes | The CPTEC city code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "atualizado_em": "string",
      "cidade": "string",
      "clima": [
        {}
      ],
      "estado": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `atualizado_em` | string |  |
| `cidade` | string |  |
| `clima` | array<object> |  |
| `estado` | string |  |

## Native endpoint

Through the native Brasil API API, this operation is `GET /cptec/v1/clima/previsao/{cityCode}` (base URL `https://brasilapi.com.br/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-city-weather-forecast.md) for the provider-specific parameters and requirements.

