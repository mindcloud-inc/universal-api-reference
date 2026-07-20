# Fliqr AI: Find Account Tag By Name

Finds an account tag in Fliqr AI by name.

```
GET https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/find-account-tag-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fliqr AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/find-account-tag-by-name?connectionId=$CONNECTION_ID&tagName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/find-account-tag-by-name?${params}`, {
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
| `tagName` | string | yes | Tag name. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Fliqr AI API, this operation is `GET /accounts/tags/name/:tag_name` (base URL `https://app.fliqr.ai/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-account-tag-by-name.md) for the provider-specific parameters and requirements.

