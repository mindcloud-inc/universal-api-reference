# TeleSign: Submit Phone Number For Intelligence



```
POST https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/submit-phone-number-for-intelligence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeleSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/submit-phone-number-for-intelligence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/submit-phone-number-for-intelligence', {
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
      "carrier": {
        "name": "Ava Chen"
      },
      "external_id": "string",
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
      "risk_insights": {
        "category": [
          1
        ]
      },
      "risk": {
        "level": "string",
        "recommendation": "string",
        "score": 1
      },
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
| `carrier.name` | string |  |
| `external_id` | string |  |
| `location.country.iso2` | string |  |
| `numbering.original.complete_phone_number` | string |  |
| `phone_type.description` | string |  |
| `reference_id` | string |  |
| `risk_insights.category` | array<number> |  |
| `risk.level` | string |  |
| `risk.recommendation` | string |  |
| `risk.score` | number |  |
| `status.code` | number |  |
| `status.description` | string |  |
| `status.updated_on` | string |  |

## Native endpoint

Through the native TeleSign API, this operation is `POST /v1/score/{complete_phone_number}` (base URL `https://rest-ww.telesign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-phone-number-for-intelligence.md) for the provider-specific parameters and requirements.

