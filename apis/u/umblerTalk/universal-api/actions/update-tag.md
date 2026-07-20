# Umbler Talk: Update Tag

Updates an existing tag in Umbler Talk.

```
PUT https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/update-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbler Talk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/update-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "organizationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/update-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "organizationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The tag ID. |
| `name` | string | no | Tag name. |
| `organizationId` | string | yes | The organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_t": "string",
      "color": "string",
      "createdAtUTC": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "emoji": "string",
      "groupIds": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "order": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_t` | string |  |
| `color` | string |  |
| `createdAtUTC` | date |  |
| `description` | string |  |
| `emoji` | string |  |
| `groupIds` | array<string> |  |
| `id` | string |  |
| `name` | string |  |
| `order` | number |  |

## Native endpoint

Through the native Umbler Talk API, this operation is `PUT /v1/tags/[:id]/` (base URL `https://app-utalk.umbler.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tag.md) for the provider-specific parameters and requirements.

