# mittwald: Get Conversation Category

Retrieves conversation category from mittwald API.

```
GET https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/get-conversation-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mittwald `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/get-conversation-category?connectionId=$CONNECTION_ID&categoryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "categoryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/get-conversation-category?${params}`, {
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
| `categoryId` | string | yes | Category ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryId": "string",
      "name": "Ava Chen",
      "referenceType": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | string |  |
| `name` | string |  |
| `referenceType` | array<string> |  |

## Native endpoint

Through the native mittwald API, this operation is `GET /v2/conversation-categories/:categoryId` (base URL `https://api.mittwald.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation-category.md) for the provider-specific parameters and requirements.

