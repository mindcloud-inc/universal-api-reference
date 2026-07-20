# Data8: Find Location

Finds location details in Data8 by postcode.

```
GET https://connect.mindcloud.co/v1/universal/data8/latest/actions/find-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Data8 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/data8/latest/actions/find-location?connectionId=$CONNECTION_ID&licence=string&postcode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "licence": "string",
  "postcode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/data8/latest/actions/find-location?${params}`, {
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
| `postcode` | string | yes | The postcode to get the location of. |
| `options` | object | no | Optional settings that control location lookup behavior. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Result": {
        "Country": "string",
        "County": "string",
        "GridReference": "string",
        "Latitude": 1,
        "Longitude": 1
      },
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
| `Result.Country` | string |  |
| `Result.County` | string |  |
| `Result.GridReference` | string |  |
| `Result.Latitude` | number |  |
| `Result.Longitude` | number |  |
| `Status.CreditsRemaining` | number |  |
| `Status.ErrorMessage` | string |  |
| `Status.Success` | boolean |  |

## Native endpoint

Through the native Data8 API, this operation is `POST /Location/FindLocation.json` (base URL `https://webservices.data-8.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-location.md) for the provider-specific parameters and requirements.

