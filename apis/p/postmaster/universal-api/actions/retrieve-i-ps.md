# Postmaster+: Retrieve IPs

Retrieves IP records from the Postmaster+ API.

```
GET https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-i-ps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmaster+ `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-i-ps?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-i-ps?${params}`, {
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
      "createdAt": "string",
      "description": "string",
      "id": "string",
      "updatedAt": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Creation timestamp. |
| `description` | string | IP description. |
| `id` | string | IP ULID. |
| `updatedAt` | string | Update timestamp. |
| `value` | string | IP value. |

## Native endpoint

Through the native Postmaster+ API, this operation is `GET /api/v1/ips` (base URL `https://postmasterplus.app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/retrieve-i-ps.md) for the provider-specific parameters and requirements.

