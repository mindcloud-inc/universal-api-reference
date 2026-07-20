# Instantly: Add Leads To Campaign Or List

Adds leads to a campaign or list in Instantly.

```
POST https://connect.mindcloud.co/v1/universal/instantly/latest/actions/add-leads-to-campaign-or-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/add-leads-to-campaign-or-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leads[]": [
    {}
  ],
  "listId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantly/latest/actions/add-leads-to-campaign-or-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leads[]": [{}],
    "listId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leads[]` | array<object> | yes | Array of lead objects to add. |
| `listId` | string | yes | List ID to add leads to. Use this or campaign ID, not both. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_leads": [
        {}
      ],
      "duplicate_email_count": 1,
      "duplicated_leads": 1,
      "in_blocklist": 1,
      "incomplete_count": 1,
      "invalid_email_count": 1,
      "leads_uploaded": 1,
      "skipped_count": 1,
      "status": "string",
      "total_sent": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_leads` | array<object> |  |
| `duplicate_email_count` | number |  |
| `duplicated_leads` | number |  |
| `in_blocklist` | number |  |
| `incomplete_count` | number |  |
| `invalid_email_count` | number |  |
| `leads_uploaded` | number |  |
| `skipped_count` | number |  |
| `status` | string |  |
| `total_sent` | number |  |

## Native endpoint

Through the native Instantly API, this operation is `POST /api/v2/leads/add` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-leads-to-campaign-or-list.md) for the provider-specific parameters and requirements.

