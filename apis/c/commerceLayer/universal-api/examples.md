# Commerce Layer Universal API Examples

These examples use the MindCloud API key and Commerce Layer connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Markets



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/list-markets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/list-markets?${params}`, {
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
      "attributes": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "external_includes": [
          "string"
        ],
        "name": "Ava Chen",
        "number": 1,
        "private": true,
        "shared_secret": "string",
        "updated_at": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "meta": {
        "mode": "string",
        "organization_id": "string",
        "trace_id": "string"
      },
      "relationships": {
        "attachments": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "base_price_list": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "customer_group": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "default_payment_method": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "default_shipping_method": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "discount_engine": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "event_stores": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "geocoder": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "inventory_model": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "merchant": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "order_validation_rules": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "price_list_schedulers": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "price_list": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "stores": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "subscription_model": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "tax_calculator": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "versions": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Markets action reference](actions/list-markets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/commerceLayer/latest/actions/list-markets).

## Create Address



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/create-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "John",
  "lastName": "Smith",
  "line1": "2883 Geraldine Lane",
  "city": "New York",
  "zipCode": "10013",
  "countryCode": "US",
  "phone": "+12126463381228"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/create-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "John",
    "lastName": "Smith",
    "line1": "2883 Geraldine Lane",
    "city": "New York",
    "zipCode": "10013",
    "countryCode": "US",
    "phone": "+12126463381228"
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
      "attributes": {
        "billing_info": "string",
        "business": true,
        "city": "string",
        "company": "string",
        "country_code": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "first_name": "Ava",
        "full_address": "string",
        "full_name": "Ava Chen",
        "is_geocoded": true,
        "is_localized": true,
        "last_name": "Chen",
        "lat": 1,
        "line_1": "string",
        "line_2": "string",
        "lng": 1,
        "map_url": "https://example.com",
        "name": "Ava Chen",
        "notes": "string",
        "phone": "string",
        "provider_name": "Ava Chen",
        "reference": "string",
        "reference_origin": "string",
        "state_code": "string",
        "static_map_url": "https://example.com",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "zip_code": "string"
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "meta": {
        "mode": "string",
        "organization_id": "string",
        "trace_id": "string"
      },
      "relationships": {
        "event_stores": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "events": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "geocoder": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "tags": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "versions": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Address action reference](actions/create-address.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/commerceLayer/latest/actions/create-address).
