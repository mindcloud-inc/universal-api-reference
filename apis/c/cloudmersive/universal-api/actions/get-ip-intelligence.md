# Cloudmersive: Get IP Intelligence

Retrieves IP intelligence from Cloudmersive.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/get-ip-intelligence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/get-ip-intelligence?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/get-ip-intelligence?${params}`, {
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
| `value` | string | no | IP address to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currencyCode": "string",
      "currencyName": "Ava Chen",
      "isBot": true,
      "isEu": true,
      "isThreat": true,
      "isTorNode": true,
      "location": {
        "countryCode": "string",
        "countryName": "Ava Chen",
        "latitude": 1,
        "longitude": 1,
        "timezoneStandardName": "Ava Chen"
      },
      "regionArea": "string",
      "subregionArea": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currencyCode` | string |  |
| `currencyName` | string |  |
| `isBot` | boolean |  |
| `isEu` | boolean |  |
| `isThreat` | boolean |  |
| `isTorNode` | boolean |  |
| `location.countryCode` | string |  |
| `location.countryName` | string |  |
| `location.latitude` | number |  |
| `location.longitude` | number |  |
| `location.timezoneStandardName` | string |  |
| `regionArea` | string |  |
| `subregionArea` | string |  |

## Native endpoint

Through the native Cloudmersive API, this operation is `POST /validate/ip/intelligence` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ip-intelligence.md) for the provider-specific parameters and requirements.

