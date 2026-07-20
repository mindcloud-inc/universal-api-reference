# Leadspicker: Get Person Communication

Retrieves communication for a person in Leadspicker.

```
GET https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/get-person-communication
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadspicker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/get-person-communication?connectionId=$CONNECTION_ID&personId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "personId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/get-person-communication?${params}`, {
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
| `personId` | number | yes | Leadspicker person identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar_url": "https://example.com",
      "connected_since": 1,
      "email_account": {},
      "linkedin_account": {},
      "messages": [
        {}
      ],
      "project_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar_url` | string |  |
| `connected_since` | number |  |
| `email_account` | object |  |
| `linkedin_account` | object |  |
| `messages` | array<object> |  |
| `project_id` | number |  |

## Native endpoint

Through the native Leadspicker API, this operation is `GET /app/sb/api/persons/:person_id/communication` (base URL `https://app.leadspicker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person-communication.md) for the provider-specific parameters and requirements.

