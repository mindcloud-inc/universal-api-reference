# WEEEK: Update Organization



```
PUT https://connect.mindcloud.co/v1/universal/wEEEK/latest/actions/update-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WEEEK `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wEEEK/latest/actions/update-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "organizationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wEEEK/latest/actions/update-organization', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "organizationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The organization name. WEEEK required this field during PATCH validation. |
| `organizationId` | string | yes | The WEEEK organization ID from the organizations API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "organization": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `organization` | object | The updated WEEEK organization. |
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native WEEEK API, this operation is `PATCH /crm/organizations/:organizationId` (base URL `https://api.weeek.net/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-organization.md) for the provider-specific parameters and requirements.

