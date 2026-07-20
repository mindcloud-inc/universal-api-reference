# FraudLabs Pro: Screen Order

Screens an order for fraud in FraudLabs Pro.

```
POST https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/screen-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FraudLabs Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/screen-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ip": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/screen-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ip": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ip` | string | yes | IP address of the online transaction. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "api_version": "string",
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
        "ip": "string",
        "is_in_blacklist": true,
        "is_proxy": true,
        "isp_name": "Ava Chen",
        "latitude": 1,
        "longitude": 1,
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
      "remaining_credits": 1,
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
| `api_version` | string |  |
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
| `ip_geolocation.ip` | string |  |
| `ip_geolocation.is_in_blacklist` | boolean |  |
| `ip_geolocation.is_proxy` | boolean |  |
| `ip_geolocation.isp_name` | string |  |
| `ip_geolocation.latitude` | number |  |
| `ip_geolocation.longitude` | number |  |
| `ip_geolocation.netspeed` | string |  |
| `ip_geolocation.proxy_type` | string |  |
| `ip_geolocation.region` | string |  |
| `ip_geolocation.timezone` | string |  |
| `ip_geolocation.usage_type[]` | array<string> |  |
| `ip_geolocation.zip_code` | string |  |
| `phone_number.is_disposable` | boolean |  |
| `phone_number.is_in_blacklist` | boolean |  |
| `remaining_credits` | number |  |
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

Through the native FraudLabs Pro API, this operation is `POST v2/order/screen` (base URL `https://api.fraudlabspro.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/screen-order.md) for the provider-specific parameters and requirements.

