# Salespanel: Log Custom Activity

Creates a custom activity in Salespanel for a visitor.

```
POST https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/log-custom-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salespanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/log-custom-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "visitorIdentifier": "string",
  "category": "string",
  "label": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/log-custom-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "visitorIdentifier": "string",
    "category": "string",
    "label": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `visitorIdentifier` | string | yes | Contact ID or email of the contact. |
| `category` | string | yes | Category for the custom activity. |
| `label` | string | yes | Label for the custom activity. |
| `activityIdentifier` | string | no | Identifier for the custom activity. |
| `metadata` | object | no | Additional data provided for the custom activity. |
| `createNew` | boolean | no | Create a new visitor if the email does not already exist. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
      "visitorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |
| `visitorId` | string |  |

## Native endpoint

Through the native Salespanel API, this operation is `POST /custom-activity/create/` (base URL `https://salespanel.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/log-custom-activity.md) for the provider-specific parameters and requirements.

