# Směnné kurzy ČNB: Get CNB PRIBOR Daily by Year and Term

Retrieves PRIBOR data for a year and term from Směnné kurzy ČNB.

```
GET https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-pribor-daily-by-year-and-term
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Směnné kurzy ČNB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-pribor-daily-by-year-and-term?connectionId=$CONNECTION_ID&period=THREE_MONTH" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "period": "THREE_MONTH"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-pribor-daily-by-year-and-term?${params}`, {
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
| `period` | string | yes | One of: `NINE_MONTH`, `ONE_DAY`, `ONE_MONTH`, `ONE_WEEK`, `ONE_YEAR`, `SIX_MONTH`, `THREE_MONTH`, `TWO_MONTH`, `TWO_WEEKS`. Example: `THREE_MONTH`. |
| `year` | number | no | Example: `2026`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pribs": [
        {
          "period": "string",
          "pribid": {},
          "pribor": 1,
          "validFor": "string"
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
| `pribs[].period` | string |  |
| `pribs[].pribid` | object |  |
| `pribs[].pribor` | number |  |
| `pribs[].validFor` | string |  |

## Native endpoint

Through the native Směnné kurzy ČNB API, this operation is `GET /pribor/daily-year-term` (base URL `https://api.cnb.cz/cnbapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cnb-pribor-daily-by-year-and-term.md) for the provider-specific parameters and requirements.

