# Let's Calendar: Upload Campaign Contacts

Uploads campaign contacts to Let's Calendar from CSV or Excel.

```
POST https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/upload-campaign-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Let's Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/upload-campaign-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/upload-campaign-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | The unique identifier of the campaign. |
| `file` | file | yes | CSV or Excel file with contact data. |
| `allowDuplicates` | boolean | no | Whether to allow duplicate emails. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "importId": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `importId` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Let's Calendar API, this operation is `POST upload-contacts` (base URL `https://panel.letscalendar.com/api/lc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-campaign-contacts.md) for the provider-specific parameters and requirements.

