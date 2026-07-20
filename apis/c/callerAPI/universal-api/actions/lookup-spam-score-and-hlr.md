# CallerAPI: Lookup Spam Score and HLR

Retrieves spam score and HLR data from CallerAPI.

```
GET https://connect.mindcloud.co/v1/universal/callerAPI/latest/actions/lookup-spam-score-and-hlr
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallerAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callerAPI/latest/actions/lookup-spam-score-and-hlr?connectionId=$CONNECTION_ID&phone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callerAPI/latest/actions/lookup-spam-score-and-hlr?${params}`, {
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
| `hlr` | boolean | no | Whether to include HLR data. |
| `phone` | string | yes | Phone number to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "business_info": {
          "business_name": "Ava Chen",
          "category": "string",
          "city": "string",
          "country": "string",
          "industry": "string",
          "state": "string",
          "verified": true
        },
        "entity_type": "string",
        "is_spam": true,
        "phone": "string",
        "reputation": "string",
        "spam_score": 1,
        "total_complaints": 1
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Lookup result payload returned by CallerAPI. |
| `data.business_info` | object | Business details when the phone number is associated with a verified business. |
| `data.business_info.business_name` | string | Verified business name for the phone number. |
| `data.business_info.category` | string | High-level business category. |
| `data.business_info.city` | string | Business city. |
| `data.business_info.country` | string | Business country code. |
| `data.business_info.industry` | string | Business industry label. |
| `data.business_info.state` | string | Business state or region. |
| `data.business_info.verified` | boolean | Whether CallerAPI verified the business information. |
| `data.entity_type` | string | Entity classification returned by CallerAPI. |
| `data.is_spam` | boolean | Whether CallerAPI classifies the phone number as spam. |
| `data.phone` | string | Normalized phone number that was looked up. |
| `data.reputation` | string | CallerAPI reputation label for the phone number. |
| `data.spam_score` | number | Numeric spam score for the phone number. |
| `data.total_complaints` | number | Total number of complaints associated with the phone number. |
| `status` | string | CallerAPI response status. |

## Native endpoint

Through the native CallerAPI API, this operation is `GET /api/lookup/:phone` (base URL `https://api.callerapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-spam-score-and-hlr.md) for the provider-specific parameters and requirements.

