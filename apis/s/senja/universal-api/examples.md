# Senja Universal API Examples

These examples use the MindCloud API key and Senja connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Testimonials

Retrieves testimonials from your Senja project.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/senja/latest/actions/list-testimonials?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/senja/latest/actions/list-testimonials?${params}`, {
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
      "testimonials": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [List Testimonials action reference](actions/list-testimonials.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/senja/latest/actions/list-testimonials).

## Create Testimonial

Creates a testimonial in your Senja project.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/senja/latest/actions/create-testimonial" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/senja/latest/actions/create-testimonial', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "id": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Testimonial action reference](actions/create-testimonial.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/senja/latest/actions/create-testimonial).
