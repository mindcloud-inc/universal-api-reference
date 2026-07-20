# xMatters: Get a site

Retrieves a site from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-site?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-site?${params}`, {
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
| `siteId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address1": "string",
      "city": "string",
      "country": "string",
      "externallyOwned": true,
      "id": "string",
      "language": "string",
      "latitude": 1,
      "links": {
        "self": "https://example.com"
      },
      "longitude": 1,
      "name": "Ava Chen",
      "postalCode": "string",
      "state": "string",
      "status": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address1` | string |  |
| `city` | string |  |
| `country` | string |  |
| `externallyOwned` | boolean |  |
| `id` | string |  |
| `language` | string |  |
| `latitude` | number |  |
| `links.self` | string |  |
| `longitude` | number |  |
| `name` | string |  |
| `postalCode` | string |  |
| `state` | string |  |
| `status` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `GET sites/{siteId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-site.md) for the provider-specific parameters and requirements.

