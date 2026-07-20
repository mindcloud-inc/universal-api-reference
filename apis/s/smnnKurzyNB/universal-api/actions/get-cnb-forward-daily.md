# Směnné kurzy ČNB: Get CNB Forward Daily

Retrieves the last valid forward rates from Směnné kurzy ČNB.

```
GET https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-forward-daily
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Směnné kurzy ČNB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-forward-daily?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-forward-daily?${params}`, {
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
      "forwardPoints": [
        {
          "ccyPair": "string",
          "forwardPoints": 1,
          "maturity": "string",
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
| `forwardPoints[].ccyPair` | string |  |
| `forwardPoints[].forwardPoints` | number |  |
| `forwardPoints[].maturity` | string |  |
| `forwardPoints[].validFor` | string |  |

## Native endpoint

Through the native Směnné kurzy ČNB API, this operation is `GET /forward/daily` (base URL `https://api.cnb.cz/cnbapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cnb-forward-daily.md) for the provider-specific parameters and requirements.

