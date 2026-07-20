# Testlify: List Coding Languages

Retrieves available coding languages from Testlify.

```
GET https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-coding-languages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-coding-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-coding-languages?${params}`, {
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
| `query` | string | no | Search text for coding languages. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "image": "string",
      "isSelected": true,
      "languageHighlightName": "Ava Chen",
      "languageId": 1,
      "name": "Ava Chen",
      "type": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `image` | string |  |
| `isSelected` | boolean |  |
| `languageHighlightName` | string |  |
| `languageId` | number |  |
| `name` | string |  |
| `type` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Testlify API, this operation is `GET /v1/assessment/coding/language` (base URL `https://api.testlify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-coding-languages.md) for the provider-specific parameters and requirements.

