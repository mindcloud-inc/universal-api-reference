# Big Cartel: Get Page

Retrieves a page from Big Cartel.

```
GET https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/get-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Big Cartel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/get-page?connectionId=$CONNECTION_ID&accountId=1&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1",
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/get-page?${params}`, {
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
| `accountId` | number | yes | The Big Cartel account ID. |
| `pageId` | string | yes | The Big Cartel page ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "category": "string",
        "content": "string",
        "isPublished": true,
        "name": "Ava Chen",
        "path": "string",
        "useLayout": true
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.category` | string |  |
| `attributes.content` | string |  |
| `attributes.isPublished` | boolean |  |
| `attributes.name` | string |  |
| `attributes.path` | string |  |
| `attributes.useLayout` | boolean |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Big Cartel API, this operation is `GET /v1/accounts/[:account-id]/pages/[:page-id]` (base URL `https://api.bigcartel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page.md) for the provider-specific parameters and requirements.

