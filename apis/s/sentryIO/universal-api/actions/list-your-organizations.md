# Sentry IO: List Your Organizations

Retrieves your organizations from Sentry IO.

```
GET https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-your-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sentry IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-your-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-your-organizations?${params}`, {
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
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "links": {},
      "name": "Ava Chen",
      "slug": "string",
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | date | Organization creation timestamp. |
| `id` | string | Organization identifier. |
| `links` | object | Organization URL metadata. |
| `name` | string | Organization name. |
| `slug` | string | Organization slug. |
| `status` | object | Organization status object. |

## Native endpoint

Through the native Sentry IO API, this operation is `GET /organizations/` (base URL `https://sentry.io/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-your-organizations.md) for the provider-specific parameters and requirements.

