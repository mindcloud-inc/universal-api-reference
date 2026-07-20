# Leadfeeder: Get Custom Feeds

Retrieves custom feeds for an account in Leadfeeder.

```
GET https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/get-custom-feeds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadfeeder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/get-custom-feeds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/get-custom-feeds?${params}`, {
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

Through the native Leadfeeder API, this operation is `GET /accounts/:accountId/custom-feeds` (base URL `https://api.leadfeeder.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-feeds.md) for the provider-specific parameters and requirements.

