# SeekTable: Backup Account Data

Retrieves a backup export from SeekTable.

```
GET https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/backup-account-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeekTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/backup-account-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/backup-account-data?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SeekTable API returns.

## Native endpoint

Through the native SeekTable API, this operation is `GET /api/account/backup` (base URL `https://www.seektable.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/backup-account-data.md) for the provider-specific parameters and requirements.

