# PIMMS: Track Lead

Creates a new tracked lead event in PIMMS.

```
POST https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/track-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PIMMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/track-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clickId": "string",
  "eventName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/track-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clickId": "string",
    "eventName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clickId` | string | yes | Unique identifier for the click event in PIMMS, typically retrieved from the 'pimms_id' browser cookie for accurate attribution. |
| `eventName` | string | yes | Name of the specific lead or conversion event you want to track (e.g., 'Sign up', 'Free Trial Registration'). |
| `externalId` | string | no | A unique identifier from your internal system (such as user ID) to link customer journeys across platforms. |
| `customerName` | string | no | Optional customer name, useful for personalized reporting and CRM integrations. |
| `customerEmail` | string | no | Customer email address to enhance CRM synchronization and facilitate personalized marketing efforts. |
| `customerAvatar` | string | no | URL to the customer's avatar image, used for richer user profiles in integrated CRM or analytics platforms. |
| `metadata` | object | no | Additional structured data or context about the lead event, aiding advanced segmentation and reporting. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "click": {},
      "customer": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `click` | object |  |
| `customer` | object |  |

## Native endpoint

Through the native PIMMS API, this operation is `POST /track/lead` (base URL `https://api.pimms.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-lead.md) for the provider-specific parameters and requirements.

