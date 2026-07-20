# Moderation API: Get Author Details

Retrieves author details from Moderation API.

```
GET https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-author-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moderation API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-author-details?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-author-details?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Either external ID or the ID assigned by moderation API. |

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

Through the native Moderation API API, this operation is `GET /authors/:id` (base URL `https://api.moderationapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-author-details.md) for the provider-specific parameters and requirements.

