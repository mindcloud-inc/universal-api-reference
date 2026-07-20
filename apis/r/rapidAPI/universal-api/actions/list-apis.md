# RapidAPI: List APIs

Retrieves APIs from RapidAPI.

```
GET https://connect.mindcloud.co/v1/universal/rapidAPI/latest/actions/list-apis
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RapidAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rapidAPI/latest/actions/list-apis?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rapidAPI/latest/actions/list-apis?${params}`, {
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
| `ownerId` | string | no | User or team ID that owns the APIs. |
| `visibility` | string | no | API visibility filter such as PUBLIC or PRIVATE. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "name": "Ava Chen",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `name` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native RapidAPI API, this operation is `GET /apis` (base URL `{{credentials.baseUrlRest}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-apis.md) for the provider-specific parameters and requirements.

