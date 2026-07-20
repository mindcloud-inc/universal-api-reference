# Quentn: Add Contact to Campaign



```
POST https://connect.mindcloud.co/v1/universal/quentn/latest/actions/add-contact-to-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quentn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quentn/latest/actions/add-contact-to-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cb_id": "123",
  "mail": "name@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quentn/latest/actions/add-contact-to-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cb_id": "123",
    "mail": "name@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cb_id` | number | yes | The numeric Quentn campaign id to trigger. Example: `123`. |
| `family_name` | string | no | Optional contact last name for the campaign trigger. |
| `first_name` | string | no | Optional contact first name for the campaign trigger. |
| `mail` | string | yes | Email address of the contact to send into the campaign. Example: `name@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The id returned by Quentn for the triggered contact or campaign entry. |
| `success` | boolean | Whether Quentn accepted the campaign trigger request. |

## Native endpoint

Through the native Quentn API, this operation is `POST /cb/:cb_id` (base URL `https://tbg6y3.us-1.quentn.com/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contact-to-campaign.md) for the provider-specific parameters and requirements.

