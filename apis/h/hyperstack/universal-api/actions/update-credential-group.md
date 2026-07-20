# Hyperstack Certificates: Update Credential Group



```
PUT https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/update-credential-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperstack Certificates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/update-credential-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "group_key": "string",
  "doesExpire": true,
  "validity": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/update-credential-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "group_key": "string",
    "doesExpire": true,
    "validity": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `badge_template` | string | no | New badge template key. |
| `blockchain` | boolean | no | Enable blockchain anchoring for credentials in this group. |
| `certificate_template` | string | no | New certificate template key. |
| `description` | string | no | Updated credential group description HTML. |
| `group_code` | string | no | Updated human-readable code for the group. |
| `group_key` | string | yes | Credential group key to update. |
| `tags` | object | no | Updated tags for the credential group. |
| `title` | string | no | Updated credential group title. |
| `url` | string | no | Updated credential group website URL. |
| `doesExpire` | boolean | yes | Whether credentials in the group expire. |
| `validity` | number | yes | Validity duration configured for the group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the credential group was updated successfully. |

## Native endpoint

Through the native Hyperstack Certificates API, this operation is `POST /group/update/:group_key` (base URL `https://api.thehyperstack.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-credential-group.md) for the provider-specific parameters and requirements.

