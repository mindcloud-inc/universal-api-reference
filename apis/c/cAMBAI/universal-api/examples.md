# CAMB.AI Universal API Examples

These examples use the MindCloud API key and CAMB.AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Voices

Retrieves all available voices from CAMB.AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/list-voices?${params}`, {
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
      "age": 1,
      "description": "string",
      "gender": 1,
      "id": 1,
      "import_counter": 1,
      "is_published": true,
      "language": 1,
      "owner": {},
      "owner_id": 1,
      "tags": [
        "string"
      ],
      "task_count": 1,
      "transcript": "string",
      "voice_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Voices action reference](actions/list-voices.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cAMBAI/latest/actions/list-voices).

## Create Audio Separation

Creates a new audio separation task in CAMB.AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/create-audio-separation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "media_file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/create-audio-separation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "media_file": "string"
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
      "task_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Audio Separation action reference](actions/create-audio-separation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cAMBAI/latest/actions/create-audio-separation).
