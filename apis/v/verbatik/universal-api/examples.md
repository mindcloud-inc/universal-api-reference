# Verbatik Universal API Examples

These examples use the MindCloud API key and Verbatik connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Voices

Retrieves a list of voices from Verbatik.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verbatik/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verbatik/latest/actions/list-voices?${params}`, {
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
      "gender": "string",
      "id": "string",
      "is_neural": true,
      "language_code": "string",
      "language_name": "Ava Chen",
      "name": "Ava Chen",
      "sample_url": "https://example.com",
      "styles": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Voices action reference](actions/list-voices.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/verbatik/latest/actions/list-voices).

## Create Custom Voice Speech

Creates speech from a cloned voice in Verbatik.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/verbatik/latest/actions/create-custom-voice-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/verbatik/latest/actions/create-custom-voice-speech', {
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

See the full [Create Custom Voice Speech action reference](actions/create-custom-voice-speech.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/verbatik/latest/actions/create-custom-voice-speech).
