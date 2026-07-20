# Golemio API: List Parking Sources

Finds parking sources in the Golemio API.

```
GET https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-parking-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Golemio API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-parking-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-parking-sources?${params}`, {
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
      "contact": {
        "email": "ava@example.com",
        "phone": "string",
        "termOfUseUrl": "https://example.com",
        "webUrl": "https://example.com"
      },
      "name": "Ava Chen",
      "source": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | object | Contact details for the parking data source. |
| `contact.email` | string | Contact email address for the source. |
| `contact.phone` | string | Contact phone number for the source. |
| `contact.termOfUseUrl` | string | Terms of use URL for the source. |
| `contact.webUrl` | string | Website URL for the source. |
| `name` | string | Display name of the parking data source. |
| `source` | string | Source identifier used by parking endpoints. |

## Native endpoint

Through the native Golemio API API, this operation is `GET /v3/parking-sources` (base URL `https://api.golemio.cz`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-parking-sources.md) for the provider-specific parameters and requirements.

