# Makeplans: Update Resource

Updates an existing resource in Makeplans.

```
PUT https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/update-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeplans `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/update-resource" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/update-resource', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `capacity` | number | no | Resource capacity. |
| `resourceId` | number | yes | The Makeplans resource ID. |
| `title` | string | no | Resource title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "capacity": 1,
      "id": 1,
      "opening_hours_mon": [
        "string"
      ],
      "opening_hours_tue": [
        "string"
      ],
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `capacity` | number |  |
| `id` | number |  |
| `opening_hours_mon` | array<string> |  |
| `opening_hours_tue` | array<string> |  |
| `title` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Makeplans API, this operation is `PUT /resources/:resourceId` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-resource.md) for the provider-specific parameters and requirements.

