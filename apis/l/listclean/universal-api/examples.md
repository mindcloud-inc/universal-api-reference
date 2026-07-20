# Listclean Universal API Examples

These examples use the MindCloud API key and Listclean connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Remaining Credits

Retrieves remaining account credits from Listclean.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/listclean/latest/actions/get-remaining-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/listclean/latest/actions/get-remaining-credits?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "credits": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Remaining Credits action reference](actions/get-remaining-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/listclean/latest/actions/get-remaining-credits).

## Start Upload

Starts a CSV upload in Listclean.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/listclean/latest/actions/start-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filename": "My file.csv",
  "file_type": "csv",
  "total_chunk_count": "24",
  "max_chunk_size": "64000",
  "email_column_index": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/listclean/latest/actions/start-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filename": "My file.csv",
    "file_type": "csv",
    "total_chunk_count": "24",
    "max_chunk_size": "64000",
    "email_column_index": "0"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "upload_id": 1
    }
  ],
  "meta": {}
}
```

See the full [Start Upload action reference](actions/start-upload.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/listclean/latest/actions/start-upload).
