# Namsor: Full Name Country

Retrieves the likely country of residence for a full name in Namsor.

```
GET https://connect.mindcloud.co/v1/universal/namsor/latest/actions/full-name-country
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Namsor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/namsor/latest/actions/full-name-country?connectionId=$CONNECTION_ID&personalNameFull=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "personalNameFull": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/namsor/latest/actions/full-name-country?${params}`, {
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
| `personalNameFull` | string | yes | Full personal name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "countriesTop": [
        "string"
      ],
      "country": "string",
      "countryAlt": "string",
      "id": "string",
      "name": "Ava Chen",
      "probabilityAltCalibrated": 1,
      "probabilityCalibrated": 1,
      "region": "string",
      "score": 1,
      "script": "string",
      "subRegion": "string",
      "topRegion": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countriesTop` | array<string> |  |
| `country` | string |  |
| `countryAlt` | string |  |
| `id` | string |  |
| `name` | string |  |
| `probabilityAltCalibrated` | number |  |
| `probabilityCalibrated` | number |  |
| `region` | string |  |
| `score` | number |  |
| `script` | string |  |
| `subRegion` | string |  |
| `topRegion` | string |  |

## Native endpoint

Through the native Namsor API, this operation is `GET /api2/json/country/:personalNameFull` (base URL `https://v2.namsor.com/NamSorAPIv2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/full-name-country.md) for the provider-specific parameters and requirements.

