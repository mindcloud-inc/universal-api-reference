# Socie: Update Group



```
PUT https://connect.mindcloud.co/v1/universal/socie/latest/actions/update-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/socie/latest/actions/update-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socie/latest/actions/update-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | yes | The Socie id or externalId of the group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isVisibleInApp": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | The group color hex code. |
| `createdAt` | date | When the group was created in Socie. |
| `id` | string | The Socie group id. |
| `isVisibleInApp` | boolean | Whether the group is visible in the Socie app. |
| `name` | string | The group name. |

## Native endpoint

Through the native Socie API, this operation is `PATCH /api/v1/groups/:identifier` (base URL `https://api.socie.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group.md) for the provider-specific parameters and requirements.

