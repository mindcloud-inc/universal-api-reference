# Kite Suite: Add or remove leads from a campaign



```
POST https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/add-or-remove-leads-from-a-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/add-or-remove-leads-from-a-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "campaign": "string",
  "leads[]": [
    "string"
  ],
  "action": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/add-or-remove-leads-from-a-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "campaign": "string",
    "leads[]": ["string"],
    "action": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `campaign` | string | yes | The ID of the campaign. |
| `leads[]` | array | yes | Array of lead IDs to add or remove. |
| `action` | string | yes | The action to perform ("add" or "remove"). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "lead": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `lead` | string |  |

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/campaign/lead` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-or-remove-leads-from-a-campaign.md) for the provider-specific parameters and requirements.

