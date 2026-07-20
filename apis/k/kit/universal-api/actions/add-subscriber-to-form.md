# Kit: Add Subscriber to Form

Adds an existing subscriber to a Kit form.

```
POST https://connect.mindcloud.co/v1/universal/kit/latest/actions/add-subscriber-to-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kit/latest/actions/add-subscriber-to-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "12345",
  "emailAddress": "subscriber@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kit/latest/actions/add-subscriber-to-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "12345",
    "emailAddress": "subscriber@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | number | yes | The ID of the form to add the subscriber to. Example: `12345`. |
| `emailAddress` | string | yes | Email address of an existing subscriber. Example: `subscriber@example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `referrer` | string | no | Optional referrer URL to attribute this subscription. Example: `https://example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "subscriber": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `subscriber` | object | Subscriber object after being added to the form. |

## Native endpoint

Through the native Kit API, this operation is `POST /forms/:form_id/subscribers` (base URL `https://api.kit.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-subscriber-to-form.md) for the provider-specific parameters and requirements.

