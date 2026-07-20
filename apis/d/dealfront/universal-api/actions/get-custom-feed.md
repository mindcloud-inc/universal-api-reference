# Dealfront: Get Custom Feed

Retrieves a custom feed from Dealfront.

```
GET https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/get-custom-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dealfront `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/get-custom-feed?connectionId=$CONNECTION_ID&accountId=1&customFeedId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1",
  "customFeedId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/get-custom-feed?${params}`, {
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
| `accountId` | number | yes | ID of the account that owns the custom feed. |
| `customFeedId` | string | yes | ID of the custom feed to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "name": "Ava Chen"
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
| `attributes.name` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Dealfront API, this operation is `GET /accounts/:account_id/custom-feeds/:custom_feed_id` (base URL `https://api.leadfeeder.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-feed.md) for the provider-specific parameters and requirements.

