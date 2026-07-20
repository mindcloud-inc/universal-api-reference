# Rebrandly: Count Links

Retrieves the number of links in Rebrandly.

```
GET https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/count-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrandly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/count-links?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/count-links?${params}`, {
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
| `favourite` | boolean | no | Filter links by favourite status. |
| `domain.id` | string | no | Filter links by branded domain ID. Example: `8f104cc5b6ee4a4ba7897b06ac2ddcfb`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of links matching the request. |

## Native endpoint

Through the native Rebrandly API, this operation is `GET /links/count` (base URL `https://api.rebrandly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-links.md) for the provider-specific parameters and requirements.

