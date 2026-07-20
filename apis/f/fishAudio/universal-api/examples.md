# Fish Audio Universal API Examples

These examples use the MindCloud API key and Fish Audio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get API Credit

Retrieves current API credit balance from Fish Audio.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/get-api-credit?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/get-api-credit?${params}`, {
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
      "_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "credit": "string",
      "has_free_credit": true,
      "has_phone_sha256": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get API Credit action reference](actions/get-api-credit.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fishAudio/latest/actions/get-api-credit).

## Create Model

Creates a new voice model in Fish Audio.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/create-model" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "voices[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/create-model', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "voices[]": ["string"]
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
      "_id": "string",
      "author": {},
      "cover_image": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "languages": [
        "string"
      ],
      "like_count": 1,
      "liked": true,
      "lock_visibility": true,
      "mark_count": 1,
      "marked": true,
      "samples": [
        {}
      ],
      "shared_count": 1,
      "state": "string",
      "tags": [
        "string"
      ],
      "task_count": 1,
      "title": "string",
      "train_mode": "string",
      "type": "string",
      "unliked": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Model action reference](actions/create-model.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fishAudio/latest/actions/create-model).
