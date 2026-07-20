# Google Slides Universal API Examples

These examples use the MindCloud API key and Google Slides connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Presentation

Retrieves a presentation from Google Slides.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/get-presentation?connectionId=$CONNECTION_ID&presentationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "presentationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/get-presentation?${params}`, {
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
      "layouts": [
        {}
      ],
      "locale": "string",
      "masters": [
        {}
      ],
      "pageSize": {},
      "presentationId": "string",
      "revisionId": "string",
      "slides": [
        {}
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Presentation action reference](actions/get-presentation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleSlides/latest/actions/get-presentation).

## Create Presentation

Creates a new presentation in Google Slides.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/create-presentation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleSlides/latest/actions/create-presentation', {
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
  "data": [
    {
      "layouts": [
        {}
      ],
      "locale": "string",
      "masters": [
        {}
      ],
      "pageSize": {},
      "presentationId": "string",
      "revisionId": "string",
      "slides": [
        {}
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Presentation action reference](actions/create-presentation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleSlides/latest/actions/create-presentation).
