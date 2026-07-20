# Směnné kurzy ČNB: Get CNB PRIBOR Daily

Retrieves the last valid PRIBOR data from Směnné kurzy ČNB.

```
GET https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-pribor-daily
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Směnné kurzy ČNB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-pribor-daily?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-pribor-daily?${params}`, {
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
| `date` | date | no | Example: `2026-04-14`. |

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

Through the native Směnné kurzy ČNB API, this operation is `GET /pribor/daily` (base URL `https://api.cnb.cz/cnbapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cnb-pribor-daily.md) for the provider-specific parameters and requirements.

