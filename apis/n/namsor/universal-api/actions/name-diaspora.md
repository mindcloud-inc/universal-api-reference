# Namsor: Name Diaspora

Retrieves the likely diaspora for a name in Namsor by country.

```
GET https://connect.mindcloud.co/v1/universal/namsor/latest/actions/name-diaspora
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Namsor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/namsor/latest/actions/name-diaspora?connectionId=$CONNECTION_ID&countryIso2=string&firstName=Ava&lastName=Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "countryIso2": "string",
  "firstName": "Ava",
  "lastName": "Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/namsor/latest/actions/name-diaspora?${params}`, {
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
| `countryIso2` | string | yes | Two-letter ISO country code. |
| `firstName` | string | yes | First name. |
| `lastName` | string | yes | Last name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "countryIso2": "string",
      "ethnicitiesTop": [
        "string"
      ],
      "ethnicity": "string",
      "ethnicityAlt": "string",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "lifted": true,
      "probabilityAltCalibrated": 1,
      "probabilityCalibrated": 1,
      "score": 1,
      "script": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countryIso2` | string |  |
| `ethnicitiesTop` | array<string> |  |
| `ethnicity` | string |  |
| `ethnicityAlt` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `lifted` | boolean |  |
| `probabilityAltCalibrated` | number |  |
| `probabilityCalibrated` | number |  |
| `score` | number |  |
| `script` | string |  |

## Native endpoint

Through the native Namsor API, this operation is `GET /api2/json/diaspora/:countryIso2/:firstName/:lastName` (base URL `https://v2.namsor.com/NamSorAPIv2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/name-diaspora.md) for the provider-specific parameters and requirements.

