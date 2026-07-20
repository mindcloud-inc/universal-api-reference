# Comm100: Get Public Canned Message Category

Retrieves a public canned message category from Comm100.

```
GET https://connect.mindcloud.co/v1/universal/comm100/latest/actions/get-public-canned-message-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Comm100 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/comm100/latest/actions/get-public-canned-message-category?connectionId=$CONNECTION_ID&publicCannedMessageCategoryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "publicCannedMessageCategoryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/comm100/latest/actions/get-public-canned-message-category?${params}`, {
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
| `publicCannedMessageCategoryId` | string | yes | The Comm100 public canned message category ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Comm100 API returns.

## Native endpoint

Through the native Comm100 API, this operation is `GET global/publicCannedMessageCategories/{{id}}` (base URL `https://api17.comm100.io/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-public-canned-message-category.md) for the provider-specific parameters and requirements.

