# FraudLabs Pro: Get Order Result

Retrieves an order result from FraudLabs Pro.

```
GET https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/get-order-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FraudLabs Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/get-order-result?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/get-order-result?${params}`, {
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
| `id` | string | yes | The FraudLabs Pro transaction ID to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billing_address": {
        "ip_distance_in_km": 1,
        "ip_distance_in_mile": 1,
        "is_ip_country_match": true
      },
      "credit_card": {
        "card_brand": "string",
        "card_issuing_bank": "string",
        "card_issuing_country": "string",
        "card_type": "string",
        "is_bin_country_match": true,
        "is_bin_exist": true,
        "is_in_blacklist": true,
        "is_prepaid": true
      },
      "device": {
        "is_in_blacklist": true,
        "is_malware_exploit": true
      },
      "email_address": {
        "is_disposable": true,
        "is_domain_exist": true,
        "is_free": true,
        "is_in_blacklist": true,
        "is_new_domain_name": true
      },
      "fraudlabspro_id": "string",
      "fraudlabspro_rules": [
        [
          "string"
        ]
      ],
      "fraudlabspro_score": 1,
      "fraudlabspro_status": "string",
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
        "proxy_type": "string",
        "region": "string",
        "timezone": "string",
        "usage_type": [
          [
            "string"
          ]
        ],
        "zip_code": "string"
      },
      "phone_number": {
        "is_disposable": true,
        "is_in_blacklist": true
      },
      "shipping_address": {
        "is_address_ship_forward": true,
        "is_bill_city_match": true,
        "is_bill_country_match": true,
        "is_bill_postcode_match": true,
        "is_bill_state_match": true,
        "is_export_controlled_country": true,
        "is_in_blacklist": true
      },
      "user_order_id": "string",
      "username": {
        "is_high_risk": true,
        "is_in_blacklist": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billing_address.ip_distance_in_km` | number |  |
| `billing_address.ip_distance_in_mile` | number |  |
| `billing_address.is_ip_country_match` | boolean |  |
| `credit_card.card_brand` | string |  |
| `credit_card.card_issuing_bank` | string |  |
| `credit_card.card_issuing_country` | string |  |
| `credit_card.card_type` | string |  |
| `credit_card.is_bin_country_match` | boolean |  |
| `credit_card.is_bin_exist` | boolean |  |
| `credit_card.is_in_blacklist` | boolean |  |
| `credit_card.is_prepaid` | boolean |  |
| `device.is_in_blacklist` | boolean |  |
| `device.is_malware_exploit` | boolean |  |
| `email_address.is_disposable` | boolean |  |
| `email_address.is_domain_exist` | boolean |  |
| `email_address.is_free` | boolean |  |
| `email_address.is_in_blacklist` | boolean |  |
| `email_address.is_new_domain_name` | boolean |  |
| `fraudlabspro_id` | string |  |
| `fraudlabspro_rules[]` | array<string> |  |
| `fraudlabspro_score` | number |  |
| `fraudlabspro_status` | string |  |
| `ip_geolocation.city` | string |  |
| `ip_geolocation.continent` | string |  |
| `ip_geolocation.country_code` | string |  |
| `ip_geolocation.country_name` | string |  |
| `ip_geolocation.domain` | string |  |
| `ip_geolocation.elevation` | number |  |
| `ip_geolocation.ip` | string |  |
| `ip_geolocation.is_in_blacklist` | boolean |  |
| `ip_geolocation.is_proxy` | boolean |  |
| `ip_geolocation.isp_name` | string |  |
| `ip_geolocation.latitude` | number |  |
| `ip_geolocation.longitude` | number |  |
| `ip_geolocation.mobile_brand` | string |  |
| `ip_geolocation.mobile_mcc` | string |  |
| `ip_geolocation.mobile_mnc` | string |  |
| `ip_geolocation.netspeed` | string |  |
| `ip_geolocation.proxy_type` | string |  |
| `ip_geolocation.region` | string |  |
| `ip_geolocation.timezone` | string |  |
| `ip_geolocation.usage_type[]` | array<string> |  |
| `ip_geolocation.zip_code` | string |  |
| `phone_number.is_disposable` | boolean |  |
| `phone_number.is_in_blacklist` | boolean |  |
| `shipping_address.is_address_ship_forward` | boolean |  |
| `shipping_address.is_bill_city_match` | boolean |  |
| `shipping_address.is_bill_country_match` | boolean |  |
| `shipping_address.is_bill_postcode_match` | boolean |  |
| `shipping_address.is_bill_state_match` | boolean |  |
| `shipping_address.is_export_controlled_country` | boolean |  |
| `shipping_address.is_in_blacklist` | boolean |  |
| `user_order_id` | string |  |
| `username.is_high_risk` | boolean |  |
| `username.is_in_blacklist` | boolean |  |

## Native endpoint

Through the native FraudLabs Pro API, this operation is `GET v2/order/result` (base URL `https://api.fraudlabspro.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-result.md) for the provider-specific parameters and requirements.

