# Understory: List Information Requests

Retrieves information requests for an experience in Understory.

```
GET https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-information-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Understory `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-information-requests?connectionId=$CONNECTION_ID&limit=25&offset=0&experienceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "experienceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-information-requests?${params}`, {
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
| `experienceId` | string | yes | The unique identifier of the experience. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "id": "string",
          "question": "string",
          "required": true,
          "scope": "string",
          "type": "string"
        }
      ],
      "next": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].id` | string |  |
| `items[].question` | string |  |
| `items[].required` | boolean |  |
| `items[].scope` | string |  |
| `items[].type` | string |  |
| `next` | string |  |

## Native endpoint

Through the native Understory API, this operation is `GET /v1/experiences/{{experienceId}}/information-requests` (base URL `https://api.understory.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-information-requests.md) for the provider-specific parameters and requirements.

