# Cloudmersive Data Validation: Check IP Threat

Checks an IP address for threats with Cloudmersive Data Validation.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/check-ip-threat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Data Validation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/check-ip-threat?connectionId=$CONNECTION_ID&value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/check-ip-threat?${params}`, {
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
| `value` | string | yes | IP address to check for threat status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "IsThreat": true,
      "ThreatType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `IsThreat` | boolean |  |
| `ThreatType` | string |  |

## Native endpoint

Through the native Cloudmersive Data Validation API, this operation is `POST /validate/ip/is-threat` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-ip-threat.md) for the provider-specific parameters and requirements.

