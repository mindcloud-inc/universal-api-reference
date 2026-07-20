# Workiz: Unassign User from Lead

Unassigns a user from a lead in Workiz.

```
PUT https://connect.mindcloud.co/v1/universal/workiz/latest/actions/unassign-user-from-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workiz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/workiz/latest/actions/unassign-user-from-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "user": "string",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workiz/latest/actions/unassign-user-from-lead', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "user": "string",
    "uuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `user` | string | yes | The user to unassign. |
| `uuid` | string | yes | The lead UUID to unassign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "leadId": "string",
      "link": "https://example.com",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `leadId` | string |  |
| `link` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Workiz API, this operation is `POST /lead/unassign/` (base URL `https://api.workiz.com/api/v1/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unassign-user-from-lead.md) for the provider-specific parameters and requirements.

