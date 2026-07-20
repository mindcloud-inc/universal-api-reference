# ChatBot: Get User Entity

Retrieves user entity details from ChatBot API.

```
GET https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/get-user-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/get-user-entity?connectionId=$CONNECTION_ID&ID=58ee2e085d033800059a3f7f" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ID": "58ee2e085d033800059a3f7f"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/get-user-entity?${params}`, {
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
| `ID` | string | yes | ChatBot entity id. Example: `58ee2e085d033800059a3f7f`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entries": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entries` | array<object> |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native ChatBot API, this operation is `GET /entities/:ID` (base URL `https://api.chatbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-entity.md) for the provider-specific parameters and requirements.

