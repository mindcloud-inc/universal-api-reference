# OTO: Check Coverage

Checks delivery coverage in the OTO API.

```
GET https://connect.mindcloud.co/v1/universal/oTO/latest/actions/check-coverage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OTO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oTO/latest/actions/check-coverage?connectionId=$CONNECTION_ID&lat=string&lon=string&city=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lat": "string",
  "lon": "string",
  "city": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oTO/latest/actions/check-coverage?${params}`, {
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
| `lat` | string | yes | Delivery latitude to check. |
| `lon` | string | yes | Delivery longitude to check. |
| `city` | string | yes | City name used in the coverage lookup. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branchCoverage": true,
      "bulletDelivery": true,
      "courierDelivery": true,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branchCoverage` | boolean |  |
| `bulletDelivery` | boolean |  |
| `courierDelivery` | boolean |  |
| `success` | boolean |  |

## Native endpoint

Through the native OTO API, this operation is `POST /checkCoverage` (base URL `https://api.tryoto.com/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-coverage.md) for the provider-specific parameters and requirements.

