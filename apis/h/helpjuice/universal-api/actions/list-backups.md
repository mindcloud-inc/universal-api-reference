# Helpjuice: List Backups

Retrieves backups from Helpjuice.

```
GET https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/list-backups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Helpjuice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/list-backups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/list-backups?${params}`, {
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
      "backups": [
        {}
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backups` | array<object> | Backup rows returned by Helpjuice. |
| `meta` | object | Pagination metadata for the backups collection. |

## Native endpoint

Through the native Helpjuice API, this operation is `GET /backups` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-backups.md) for the provider-specific parameters and requirements.

