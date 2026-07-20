# Data8: Geocode Address

Geocodes a submitted address with Data8.

```
GET https://connect.mindcloud.co/v1/universal/data8/latest/actions/geocode-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Data8 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/data8/latest/actions/geocode-address?connectionId=$CONNECTION_ID&licence=string&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "licence": "string",
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/data8/latest/actions/geocode-address?${params}`, {
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
| `licence` | string | yes | The licence type under which you are accessing the service. |
| `name` | string | yes | The address or place name to geocode. |
| `options` | object | no | Optional settings that control geocoding behavior. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Results": [
        {
          "Country": "string",
          "Description": "string",
          "GridReference": "string",
          "Latitude": 1,
          "Longitude": 1
        }
      ],
      "Status": {
        "CreditsRemaining": 1,
        "ErrorMessage": "string",
        "Success": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Results[].Country` | string |  |
| `Results[].Description` | string |  |
| `Results[].GridReference` | string |  |
| `Results[].Latitude` | number |  |
| `Results[].Longitude` | number |  |
| `Status.CreditsRemaining` | number |  |
| `Status.ErrorMessage` | string |  |
| `Status.Success` | boolean |  |

## Native endpoint

Through the native Data8 API, this operation is `POST /Location/Geocode.json` (base URL `https://webservices.data-8.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/geocode-address.md) for the provider-specific parameters and requirements.

