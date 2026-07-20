# TeleSign: Request Phone Number Info



```
POST https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/request-phone-number-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeleSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/request-phone-number-info" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/request-phone-number-info', {
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
      "age_verify": {
        "age_verified": true
      },
      "blocklisting": {
        "blocked": true
      },
      "carrier": {
        "name": "Ava Chen"
      },
      "location": {
        "country": {
          "iso2": "string"
        }
      },
      "numbering": {
        "original": {
          "complete_phone_number": "string"
        }
      },
      "phone_type": {
        "description": "string"
      },
      "reference_id": "string",
      "status": {
        "code": 1,
        "description": "string",
        "updated_on": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `age_verify.age_verified` | boolean |  |
| `blocklisting.blocked` | boolean |  |
| `carrier.name` | string |  |
| `location.country.iso2` | string |  |
| `numbering.original.complete_phone_number` | string |  |
| `phone_type.description` | string |  |
| `reference_id` | string |  |
| `status.code` | number |  |
| `status.description` | string |  |
| `status.updated_on` | string |  |

## Native endpoint

Through the native TeleSign API, this operation is `POST /v1/phoneid` (base URL `https://rest-ww.telesign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-phone-number-info.md) for the provider-specific parameters and requirements.

