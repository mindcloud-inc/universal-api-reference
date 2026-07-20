# Livestorm: Register Session Person

Registers a person for a session in Livestorm.

```
POST https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/register-session-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Livestorm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/register-session-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/register-session-person', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Session ID |
| `data.attributes.fields[]` | array<object> | no |  |
| `data.attributes.fields[].id` | string | no |  |
| `data.attributes.fields[].value` | string | no |  |
| `data.attributes.referrer` | string | no |  |
| `data.attributes.utmSource` | string | no |  |
| `data.attributes.utmMedium` | string | no |  |
| `data.attributes.utmTerm` | string | no |  |
| `data.attributes.utmContent` | string | no |  |
| `data.attributes.utmCampaign` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "avatarLink": "https://example.com",
        "createdAt": 1,
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "role": "string",
        "timezone": "string",
        "updatedAt": 1
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.avatarLink` | string |  |
| `attributes.createdAt` | number |  |
| `attributes.email` | string |  |
| `attributes.firstName` | string |  |
| `attributes.lastName` | string |  |
| `attributes.role` | string |  |
| `attributes.timezone` | string |  |
| `attributes.updatedAt` | number |  |
| `id` | string | ID |
| `type` | string | Type |

## Native endpoint

Through the native Livestorm API, this operation is `POST sessions/:id/people` (base URL `https://api.livestorm.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-session-person.md) for the provider-specific parameters and requirements.

