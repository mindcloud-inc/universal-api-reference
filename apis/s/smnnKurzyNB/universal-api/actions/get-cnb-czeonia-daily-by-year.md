# Směnné kurzy ČNB: Get CNB Czeonia Daily by Year

Retrieves CZEONIA rates for a year from Směnné kurzy ČNB.

```
GET https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-czeonia-daily-by-year
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Směnné kurzy ČNB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-czeonia-daily-by-year?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-czeonia-daily-by-year?${params}`, {
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
| `year` | number | no | Example: `2026`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rates": [
        {
          "rate": 1,
          "validFor": "string",
          "volumeInCZKmio": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rates[].rate` | number |  |
| `rates[].validFor` | string |  |
| `rates[].volumeInCZKmio` | number |  |

## Native endpoint

Through the native Směnné kurzy ČNB API, this operation is `GET /czeonia/daily-year` (base URL `https://api.cnb.cz/cnbapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cnb-czeonia-daily-by-year.md) for the provider-specific parameters and requirements.

