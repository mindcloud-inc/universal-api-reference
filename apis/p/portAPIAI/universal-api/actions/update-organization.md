# Port API AI: Update Organization

Updates organization details in Port.

```
PUT https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-organization', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Organization description |
| `name` | string | yes | Organization name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true,
      "organization": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |
| `organization` | object |  |

## Native endpoint

Through the native Port API AI API, this operation is `PATCH /organization` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-organization.md) for the provider-specific parameters and requirements.

