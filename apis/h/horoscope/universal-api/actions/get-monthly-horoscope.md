# Horoscope: Get Monthly Horoscope



```
GET https://connect.mindcloud.co/v1/universal/horoscope/latest/actions/get-monthly-horoscope
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Horoscope `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/horoscope/latest/actions/get-monthly-horoscope?connectionId=$CONNECTION_ID&sign=aquarius" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sign": "aquarius"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/horoscope/latest/actions/get-monthly-horoscope?${params}`, {
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
| `sign` | list<string> | yes | Required zodiac sign. One of: `aquarius`, `aries`, `cancer`, `capricorn`, `gemini`, `leo`, `libra`, `pisces`, `sagittarius`, `scorpio`, `taurus`, `virgo`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Horoscope payload containing date, period, sign, and horoscope text. |

## Native endpoint

Through the native Horoscope API, this operation is `GET /api/v1/get-horoscope/monthly` (base URL `https://freehoroscopeapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-monthly-horoscope.md) for the provider-specific parameters and requirements.

