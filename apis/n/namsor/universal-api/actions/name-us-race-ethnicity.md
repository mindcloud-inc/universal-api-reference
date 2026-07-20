# Namsor: Name US Race Ethnicity

Retrieves likely US race and ethnicity for a name in Namsor.

```
GET https://connect.mindcloud.co/v1/universal/namsor/latest/actions/name-us-race-ethnicity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Namsor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/namsor/latest/actions/name-us-race-ethnicity?connectionId=$CONNECTION_ID&firstName=Ava&lastName=Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "firstName": "Ava",
  "lastName": "Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/namsor/latest/actions/name-us-race-ethnicity?${params}`, {
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
| `firstName` | string | yes | First name. |
| `lastName` | string | yes | Last name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "probabilityAltCalibrated": 1,
      "probabilityCalibrated": 1,
      "raceEthnicitiesTop": [
        "string"
      ],
      "raceEthnicity": "string",
      "raceEthnicityAlt": "string",
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
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `probabilityAltCalibrated` | number |  |
| `probabilityCalibrated` | number |  |
| `raceEthnicitiesTop` | array<string> |  |
| `raceEthnicity` | string |  |
| `raceEthnicityAlt` | string |  |
| `score` | number |  |
| `script` | string |  |

## Native endpoint

Through the native Namsor API, this operation is `GET /api2/json/usRaceEthnicity/:firstName/:lastName` (base URL `https://v2.namsor.com/NamSorAPIv2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/name-us-race-ethnicity.md) for the provider-specific parameters and requirements.

