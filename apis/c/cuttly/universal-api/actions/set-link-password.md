# Cutt.ly: Set Link Password

Sets or removes a password for a shortened link in Cutt.ly.

```
PUT https://connect.mindcloud.co/v1/universal/cuttly/latest/actions/set-link-password
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cutt.ly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cuttly/latest/actions/set-link-password" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "edit": "string",
  "password": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cuttly/latest/actions/set-link-password', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "edit": "string",
    "password": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `edit` | string | yes | The short link to edit. |
| `password` | string | yes | Password to set. Leave blank to remove the password. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number | Provider status code for the operation. |

## Native endpoint

Through the native Cutt.ly API, this operation is `POST /api.php` (base URL `https://cutt.ly/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-link-password.md) for the provider-specific parameters and requirements.

