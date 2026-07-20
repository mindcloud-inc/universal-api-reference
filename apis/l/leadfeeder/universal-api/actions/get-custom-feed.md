# Leadfeeder: Get Custom Feed

Retrieves a specific custom feed from Leadfeeder.

```
GET https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/get-custom-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadfeeder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/get-custom-feed?connectionId=$CONNECTION_ID&customFeedId=all_leads" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customFeedId": "all_leads"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/get-custom-feed?${params}`, {
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
| `customFeedId` | string | yes | Example: `all_leads`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "criteria": [
          {}
        ],
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
| `attributes.criteria` | array<object> |  |
| `attributes.name` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Leadfeeder API, this operation is `GET /accounts/:accountId/custom-feeds/:customFeedId` (base URL `https://api.leadfeeder.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-feed.md) for the provider-specific parameters and requirements.

