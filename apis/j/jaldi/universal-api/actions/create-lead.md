# Jaldi: Create Lead

Creates a new lead in Jaldi.

```
POST https://connect.mindcloud.co/v1/universal/jaldi/latest/actions/create-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jaldi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jaldi/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "firstName": "Ava",
  "phone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jaldi/latest/actions/create-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "firstName": "Ava",
    "phone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | The Jaldi campaign_id that should receive the new lead. |
| `firstName` | string | yes | Lead first name. |
| `phone` | string | yes | Lead phone number in Jaldi's recommended +CountryCode format. |
| `lastName` | string | no | Lead last name. |
| `email` | string | no | Lead email address. |
| `notes` | string | no | Optional notes sent with the lead. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {
        "message": "string",
        "status_code": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response.message` | string | Jaldi success message returned after the lead is inserted and distributed. |
| `response.status_code` | number | HTTP-like status code returned inside Jaldi's response payload. |

## Native endpoint

Through the native Jaldi API, this operation is `POST /add_on/webhook/add` (base URL `https://api.jalditech.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead.md) for the provider-specific parameters and requirements.

