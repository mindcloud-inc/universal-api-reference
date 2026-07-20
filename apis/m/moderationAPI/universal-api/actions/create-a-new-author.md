# Moderation API: Create A New Author

Creates a new author in Moderation API.

```
POST https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/create-a-new-author
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moderation API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/create-a-new-author" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "external_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/create-a-new-author', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "external_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Author name or identifier |
| `external_id` | string | yes | External ID of the user, typically the ID of the author in your database. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `profile_picture` | string | no | URL of the author's profile picture |
| `external_link` | string | no | URL of the author's external profile |
| `email` | string | no | Author email address |
| `company` | string | no | The author's company or organization |
| `metadata` | object | no | Additional metadata provided by your system. We recommend including any relevant information that may assist in the moderation process. |
| `first_seen` | number | no | Timestamp when author first appeared |
| `last_seen` | number | no | Timestamp of last activity |
| `manual_trust_level` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "block": {},
      "company": "string",
      "email": "ava@example.com",
      "external_id": "string",
      "external_link": "https://example.com",
      "first_seen": 1,
      "id": "string",
      "last_incident": 1,
      "last_seen": 1,
      "metadata": {},
      "metrics": {},
      "name": "Ava Chen",
      "profile_picture": "string",
      "risk_evaluation": {},
      "status": "string",
      "trust_level": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `block` | object |  |
| `company` | string |  |
| `email` | string |  |
| `external_id` | string |  |
| `external_link` | string |  |
| `first_seen` | number | Timestamp when author first appeared |
| `id` | string | Author ID in Moderation API |
| `last_incident` | number |  |
| `last_seen` | number | Timestamp of last activity |
| `metadata` | object | Additional metadata provided by your system. We recommend including any relevant information that may assist in the moderation process. |
| `metrics` | object |  |
| `name` | string |  |
| `profile_picture` | string |  |
| `risk_evaluation` | object |  |
| `status` | string | Current author status |
| `trust_level` | object |  |

## Native endpoint

Through the native Moderation API API, this operation is `POST /authors` (base URL `https://api.moderationapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-new-author.md) for the provider-specific parameters and requirements.

