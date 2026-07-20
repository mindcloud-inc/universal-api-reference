# JmpTo: Update Campaign

Updates an existing campaign in JmpTo.

```
PUT https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JmpTo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/update-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Campaign ID to update. |
| `slug` | string | no | Rotator slug. |
| `name` | string | yes | Campaign name. |
| `public` | boolean | no | Campaign access flag. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": "string",
      "error": 1,
      "id": 1,
      "list": "https://example.com",
      "public": true,
      "rotator": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | string | Campaign name. |
| `error` | number | Provider success/error code. |
| `id` | number | Campaign ID. |
| `list` | string | Campaign list URL. |
| `public` | boolean | Whether the campaign is public. |
| `rotator` | string | Campaign rotator URL. |

## Native endpoint

Through the native JmpTo API, this operation is `PUT /campaign/:id/update` (base URL `https://jmpto.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.

