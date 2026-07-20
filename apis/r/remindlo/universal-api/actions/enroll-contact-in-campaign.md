# Remindlo: Enroll Contact In Campaign



```
POST https://connect.mindcloud.co/v1/universal/remindlo/latest/actions/enroll-contact-in-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Remindlo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/remindlo/latest/actions/enroll-contact-in-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/remindlo/latest/actions/enroll-contact-in-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes |  |
| `contactId` | string | no |  |
| `customerId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enrollment_id": "string",
      "reason": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enrollment_id` | string |  |
| `reason` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Remindlo API, this operation is `POST /campaigns-enroll` (base URL `https://api.remindlo.co.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enroll-contact-in-campaign.md) for the provider-specific parameters and requirements.

