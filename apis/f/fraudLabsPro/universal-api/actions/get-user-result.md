# FraudLabs Pro: Get User Result

Retrieves a user result from FraudLabs Pro.

```
GET https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/get-user-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FraudLabs Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/get-user-result?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/get-user-result?${params}`, {
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
| `id` | string | yes | The FraudLabs Pro user transaction ID or merchant user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "device": {
        "browser": "string",
        "device_type": "string",
        "is_in_blacklist": true,
        "is_malware_exploit": true,
        "operating_system": "string"
      },
      "email_address": {
        "is_disposable": true,
        "is_domain_exists": true,
        "is_free": true,
        "is_in_blacklist": true,
        "is_new_domain_name": true
      },
      "ip_geolocation": {
        "city": "string",
        "continent": "string",
        "country_code": "string",
        "country_name": "Ava Chen",
        "domain": "string",
        "elevation": 1,
        "ip": "string",
        "is_in_blacklist": true,
        "is_proxy": true,
        "isp_name": "Ava Chen",
        "latitude": 1,
        "longitude": 1,
        "mobile_brand": "string",
        "mobile_mcc": "string",
        "mobile_mnc": "string",
        "netspeed": "string",
        "region": "string",
        "timezone": "string",
        "usage_type": "string",
        "zip_code": "string"
      },
      "phone_number": {
        "is_disposable": true,
        "is_in_blacklist": true
      },
      "user_score": 1,
      "user_transaction_id": "string",
      "user_transaction_rules": [
        [
          "string"
        ]
      ],
      "user_transaction_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `device.browser` | string | The browser name and version. |
| `device.device_type` | string | The type of the associated device. |
| `device.is_in_blacklist` | boolean | Whether the device ID is in the blacklist database. |
| `device.is_malware_exploit` | boolean | Whether the machine is infected. |
| `device.operating_system` | string | The operating system name. |
| `email_address.is_disposable` | boolean | Whether the email is disposable. |
| `email_address.is_domain_exists` | boolean | Whether the email domain exists. |
| `email_address.is_free` | boolean | Whether the email is from a free email provider. |
| `email_address.is_in_blacklist` | boolean | Whether the email address is in the blacklist database. |
| `email_address.is_new_domain_name` | boolean | Whether the email domain name is newly registered. |
| `ip_geolocation.city` | string | Estimated city of the IP address. |
| `ip_geolocation.continent` | string | Estimated continent of the IP address. |
| `ip_geolocation.country_code` | string | Estimated ISO-3166 alpha-2 country code of the IP address. |
| `ip_geolocation.country_name` | string | Estimated country of the IP address. |
| `ip_geolocation.domain` | string | Estimated domain name of the IP address. |
| `ip_geolocation.elevation` | number | Estimated elevation of the IP address. |
| `ip_geolocation.ip` | string | IP address of the transaction. |
| `ip_geolocation.is_in_blacklist` | boolean | Whether the IP address is in the blacklist database. |
| `ip_geolocation.is_proxy` | boolean | Whether the IP address is from a known anonymous proxy server. |
| `ip_geolocation.isp_name` | string | Estimated ISP name of the IP address. |
| `ip_geolocation.latitude` | number | Estimated latitude of the IP address. |
| `ip_geolocation.longitude` | number | Estimated longitude of the IP address. |
| `ip_geolocation.mobile_brand` | string | Estimated mobile brand information of the IP address. |
| `ip_geolocation.mobile_mcc` | string | Estimated mobile MCC information of the IP address. |
| `ip_geolocation.mobile_mnc` | string | Estimated mobile MNC information of the IP address. |
| `ip_geolocation.netspeed` | string | Estimated netspeed of the IP address. |
| `ip_geolocation.region` | string | Estimated region of the IP address. |
| `ip_geolocation.timezone` | string | Estimated timezone of the IP address. |
| `ip_geolocation.usage_type` | string | Estimated usage type of the IP address. |
| `ip_geolocation.zip_code` | string | Estimated ZIP code of the IP address. |
| `phone_number.is_disposable` | boolean | Whether the phone number is disposable. |
| `phone_number.is_in_blacklist` | boolean | Whether the user's phone number is in the blacklist database. |
| `user_score` | number | Overall score between 1 and 100. |
| `user_transaction_id` | string | System unique identifier for this API transaction. |
| `user_transaction_rules[]` | array<string> | Rules triggered by the system. |
| `user_transaction_status` | string | Final action based on the rules analysis. |

## Native endpoint

Through the native FraudLabs Pro API, this operation is `GET v2/user/result` (base URL `https://api.fraudlabspro.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-result.md) for the provider-specific parameters and requirements.

