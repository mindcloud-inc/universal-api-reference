# DONNAJAMES Easy: Fetch All Chatbots

Retrieves all chatbots from DONNAJAMES Easy.

```
GET https://connect.mindcloud.co/v1/universal/dONNAJAMESEasy/latest/actions/fetch-all-chatbots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DONNAJAMES Easy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dONNAJAMESEasy/latest/actions/fetch-all-chatbots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dONNAJAMESEasy/latest/actions/fetch-all-chatbots?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "meta": {},
      "modified_at": "string",
      "name": "Ava Chen",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `meta` | object |  |
| `modified_at` | string |  |
| `name` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native DONNAJAMES Easy API, this operation is `GET chatbots` (base URL `https://app.gpt-trainer.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-all-chatbots.md) for the provider-specific parameters and requirements.

