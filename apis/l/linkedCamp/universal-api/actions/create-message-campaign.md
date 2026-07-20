# LinkedCamp: Create Message Campaign



```
POST https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/create-message-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkedCamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/create-message-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "message1": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/create-message-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "message1": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Campaign title. |
| `url` | string | no | Optional LinkedIn search URL used as the campaign source. |
| `message1` | string | yes | First message. |
| `message2` | string | no | Optional second follow-up message. |
| `message3` | string | no | Optional third follow-up message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | string | Created campaign identifier. |
| `message` | string | LinkedCamp status message. |
| `success` | boolean | Whether LinkedCamp created the campaign successfully. |

## Native endpoint

Through the native LinkedCamp API, this operation is `POST /campaigns` (base URL `https://api.linkedcamp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-message-campaign.md) for the provider-specific parameters and requirements.

