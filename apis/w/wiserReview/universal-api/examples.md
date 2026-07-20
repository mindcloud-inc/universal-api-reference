# WiserReview Universal API Examples

These examples use the MindCloud API key and WiserReview connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Reviews

Retrieves reviews from WiserReview.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wiserReview/latest/actions/list-reviews?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wiserReview/latest/actions/list-reviews?${params}`, {
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
      "arrimg": [
        "string"
      ],
      "arrvdo": [
        "string"
      ],
      "cn": "string",
      "createdAt": "string",
      "ct": "string",
      "e": "string",
      "Id": "string",
      "ircmnd": true,
      "ivrfd": true,
      "rtng": 1,
      "rttl": "string",
      "rtxt": "string",
      "st": "string",
      "udt": "string",
      "un": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Reviews action reference](actions/list-reviews.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wiserReview/latest/actions/list-reviews).

## Create Review

Creates a new review in WiserReview.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wiserReview/latest/actions/create-review" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wiserReview/latest/actions/create-review', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Create Review action reference](actions/create-review.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wiserReview/latest/actions/create-review).
