# Blueink: Retrieve Person

Retrieves an existing person from Blueink.

```
GET https://connect.mindcloud.co/v1/universal/blueink/latest/actions/retrieve-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blueink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueink/latest/actions/retrieve-person?connectionId=$CONNECTION_ID&personId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "personId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueink/latest/actions/retrieve-person?${params}`, {
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
| `personId` | string | yes | Person ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channels": [
        {
          "email": "ava@example.com",
          "id": "string",
          "kind": "string",
          "phone": "string"
        }
      ],
      "id": "string",
      "isUser": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels[].email` | string |  |
| `channels[].id` | string |  |
| `channels[].kind` | string |  |
| `channels[].phone` | string |  |
| `id` | string |  |
| `isUser` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Blueink API, this operation is `GET /persons/:personId/` (base URL `https://api.blueink.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-person.md) for the provider-specific parameters and requirements.

