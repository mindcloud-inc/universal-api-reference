# FraudLabs Pro Universal API Examples

These examples use the MindCloud API key and FraudLabs Pro connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Order Result

Retrieves an order result from FraudLabs Pro.

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

Example response:

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

See the full [Get Order Result action reference](actions/get-order-result.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fraudLabsPro/latest/actions/get-order-result).

## Feedback Order

Updates order feedback in FraudLabs Pro.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/feedback-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "action": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/feedback-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "action": "0"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "fraudlabspro_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Feedback Order action reference](actions/feedback-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fraudLabsPro/latest/actions/feedback-order).
