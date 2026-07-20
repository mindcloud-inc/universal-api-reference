# Namsor: Name Origin

Retrieves the likely country of origin for a name in Namsor.

```
GET https://connect.mindcloud.co/v1/universal/namsor/latest/actions/name-origin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Namsor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/namsor/latest/actions/name-origin?connectionId=$CONNECTION_ID&firstName=Ava&lastName=Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "firstName": "Ava",
  "lastName": "Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/namsor/latest/actions/name-origin?${params}`, {
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
      "countriesOriginTop": [
        "string"
      ],
      "countryOrigin": "string",
      "countryOriginAlt": "string",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "probabilityAltCalibrated": 1,
      "probabilityCalibrated": 1,
      "regionOrigin": "string",
      "score": 1,
      "script": "string",
      "subRegionOrigin": "string",
      "topRegionOrigin": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countriesOriginTop` | array<string> |  |
| `countryOrigin` | string |  |
| `countryOriginAlt` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `probabilityAltCalibrated` | number |  |
| `probabilityCalibrated` | number |  |
| `regionOrigin` | string |  |
| `score` | number |  |
| `script` | string |  |
| `subRegionOrigin` | string |  |
| `topRegionOrigin` | string |  |

## Native endpoint

Through the native Namsor API, this operation is `GET /api2/json/origin/:firstName/:lastName` (base URL `https://v2.namsor.com/NamSorAPIv2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/name-origin.md) for the provider-specific parameters and requirements.

