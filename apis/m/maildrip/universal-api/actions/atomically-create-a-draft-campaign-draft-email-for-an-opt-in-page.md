# Maildrip: Atomically create a draft campaign + draft email for an opt-in page



```
POST https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/atomically-create-a-draft-campaign-draft-email-for-an-opt-in-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/atomically-create-a-draft-campaign-draft-email-for-an-opt-in-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": "string",
  "campaignName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/atomically-create-a-draft-campaign-draft-email-for-an-opt-in-page', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": "string",
    "campaignName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageId` | string | yes |  |
| `campaignName` | string | yes |  |
| `emailSubject` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Campaign and draft email created |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/opt-in-pages/{pageId}/quick-campaign` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/atomically-create-a-draft-campaign-draft-email-for-an-opt-in-page.md) for the provider-specific parameters and requirements.

