# Prembly: Advance Phone Number

Creates an advanced phone number verification in Prembly.

```
POST https://connect.mindcloud.co/v1/universal/prembly/latest/actions/advance-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/advance-phone-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prembly/latest/actions/advance-phone-number', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "blocklisting": {
        "block_code": 1,
        "block_description": "string",
        "blocked": true
      },
      "carrier": {
        "name": "Ava Chen"
      },
      "contact": {
        "address1": "string",
        "address2": "string",
        "address3": "string",
        "address4": "string",
        "city": "string",
        "country": "string",
        "date_of_birth": "2026-05-07T12:00:00.000Z",
        "email_address": "ava@example.com",
        "first_name": "Ava",
        "last_name": "Chen",
        "state_province": "string",
        "status": {
          "code": 1,
          "description": "string"
        },
        "zip_postal_code": "string"
      },
      "location": {
        "city": "string",
        "coordinates": {
          "latitude": 1,
          "longitude": 1
        },
        "country": {
          "iso2": "string",
          "iso3": "string",
          "name": "Ava Chen"
        },
        "county": "string",
        "metro_code": "string",
        "state": "string",
        "time_zone": {
          "name": "Ava Chen",
          "utc_offset_max": "string",
          "utc_offset_min": "string"
        },
        "zip": "string"
      },
      "numbering": {
        "cleansing": {
          "call": {
            "cleansed_code": 1,
            "country_code": "string",
            "max_length": 1,
            "min_length": 1,
            "phone_number": "string"
          },
          "sms": {
            "cleansed_code": 1,
            "country_code": "string",
            "max_length": 1,
            "min_length": 1,
            "phone_number": "string"
          }
        },
        "original": {
          "complete_phone_number": "string",
          "country_code": "string",
          "phone_number": "string"
        }
      },
      "phone_type": {
        "code": "string",
        "description": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocklisting.block_code` | number |  |
| `blocklisting.block_description` | string |  |
| `blocklisting.blocked` | boolean |  |
| `carrier.name` | string |  |
| `contact.address1` | string |  |
| `contact.address2` | string |  |
| `contact.address3` | string |  |
| `contact.address4` | string |  |
| `contact.city` | string |  |
| `contact.country` | string |  |
| `contact.date_of_birth` | date |  |
| `contact.email_address` | string |  |
| `contact.first_name` | string |  |
| `contact.last_name` | string |  |
| `contact.state_province` | string |  |
| `contact.status.code` | number |  |
| `contact.status.description` | string |  |
| `contact.zip_postal_code` | string |  |
| `location.city` | string |  |
| `location.coordinates.latitude` | number |  |
| `location.coordinates.longitude` | number |  |
| `location.country.iso2` | string |  |
| `location.country.iso3` | string |  |
| `location.country.name` | string |  |
| `location.county` | string |  |
| `location.metro_code` | string |  |
| `location.state` | string |  |
| `location.time_zone.name` | string |  |
| `location.time_zone.utc_offset_max` | string |  |
| `location.time_zone.utc_offset_min` | string |  |
| `location.zip` | string |  |
| `numbering.cleansing.call.cleansed_code` | number |  |
| `numbering.cleansing.call.country_code` | string |  |
| `numbering.cleansing.call.max_length` | number |  |
| `numbering.cleansing.call.min_length` | number |  |
| `numbering.cleansing.call.phone_number` | string |  |
| `numbering.cleansing.sms.cleansed_code` | number |  |
| `numbering.cleansing.sms.country_code` | string |  |
| `numbering.cleansing.sms.max_length` | number |  |
| `numbering.cleansing.sms.min_length` | number |  |
| `numbering.cleansing.sms.phone_number` | string |  |
| `numbering.original.complete_phone_number` | string |  |
| `numbering.original.country_code` | string |  |
| `numbering.original.phone_number` | string |  |
| `phone_type.code` | string |  |
| `phone_type.description` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `POST /verification/phone_number/advance` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/advance-phone-number.md) for the provider-specific parameters and requirements.

