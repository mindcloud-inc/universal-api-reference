# Brasil API: Get Airport Weather Conditions

Retrieves current airport weather conditions from Brasil API by ICAO code.

```
GET https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-airport-weather-conditions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brasil API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-airport-weather-conditions?connectionId=$CONNECTION_ID&icaoCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "icaoCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-airport-weather-conditions?${params}`, {
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
| `icaoCode` | string | yes | The 4-letter ICAO airport code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "atualizado_em": "string",
      "codigo_icao": "string",
      "condicao": "string",
      "condicao_desc": "string",
      "direcao_vento": 1,
      "pressao_atmosferica": 1,
      "temp": 1,
      "umidade": 1,
      "vento": 1,
      "visibilidade": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `atualizado_em` | string |  |
| `codigo_icao` | string |  |
| `condicao` | string |  |
| `condicao_desc` | string |  |
| `direcao_vento` | number |  |
| `pressao_atmosferica` | number |  |
| `temp` | number |  |
| `umidade` | number |  |
| `vento` | number |  |
| `visibilidade` | string |  |

## Native endpoint

Through the native Brasil API API, this operation is `GET /cptec/v1/clima/aeroporto/{icaoCode}` (base URL `https://brasilapi.com.br/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-airport-weather-conditions.md) for the provider-specific parameters and requirements.

