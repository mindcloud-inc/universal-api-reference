# Systeme.io: List Enrollments

Retrieves the collection of enrollments from Systeme.io.

```
GET https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/list-enrollments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Systeme.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/list-enrollments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/list-enrollments?${params}`, {
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
      "hasMore": true,
      "items": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasMore` | boolean | Whether more pages are available. |
| `items` | array<object> | Enrollment records. |

## Native endpoint

Through the native Systeme.io API, this operation is `GET /api/school/enrollments` (base URL `https://api.systeme.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-enrollments.md) for the provider-specific parameters and requirements.

