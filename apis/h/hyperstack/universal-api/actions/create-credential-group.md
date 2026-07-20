# Hyperstack Certificates: Create Credential Group



```
POST https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/create-credential-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperstack Certificates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/create-credential-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "blockchain": true,
  "description": "string",
  "does_expire": true,
  "group_code": "string",
  "tags": {},
  "title": "string",
  "url": "https://example.com",
  "validity": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/create-credential-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "blockchain": true,
    "description": "string",
    "does_expire": true,
    "group_code": "string",
    "tags": {},
    "title": "string",
    "url": "https://example.com",
    "validity": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `badge_template` | string | no | Badge template key. |
| `blockchain` | boolean | yes | Enable blockchain anchoring for credentials. |
| `certificate_template` | string | no | Certificate template key. |
| `description` | string | yes | Description of the credential group. |
| `does_expire` | boolean | yes | Whether credentials in this group expire. |
| `group_code` | string | yes | Human-readable code for the group. |
| `tags` | object | yes | Tags related to the credential group. |
| `title` | string | yes | Title of the credential group. |
| `url` | string | yes | External URL associated with the credential group. |
| `validity` | number | yes | Validity period in years when does_expire is true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "group_key": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `group_key` | string | The unique key assigned to the newly created credential group. |
| `success` | boolean | Indicates whether the group creation was successful. |

## Native endpoint

Through the native Hyperstack Certificates API, this operation is `POST /groups/new` (base URL `https://api.thehyperstack.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-credential-group.md) for the provider-specific parameters and requirements.

