# LinkedCamp: Create Campaign



```
POST https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkedCamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "sequence": "string",
  "content": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "sequence": "string",
    "content": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Campaign title. |
| `url` | string | no | Optional URL associated with the campaign. |
| `sequence` | string | yes | Campaign sequence type, such as CONNECT, MESSAGE, INMAIL, or EMAIL. |
| `content` | object | yes | Campaign content object matching the selected sequence type. |

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
| `message` | string | Provider response message. |
| `success` | boolean | Whether the campaign was created. |

## Native endpoint

Through the native LinkedCamp API, this operation is `POST /campaigns/` (base URL `https://api.linkedcamp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

