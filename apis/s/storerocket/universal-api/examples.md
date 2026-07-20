# Storerocket Universal API Examples

These examples use the MindCloud API key and Storerocket connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Info



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storerocket/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storerocket/latest/actions/get-user-info?${params}`, {
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
      "company": "string",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "profilePhotoUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get User Info action reference](actions/get-user-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/storerocket/latest/actions/get-user-info).

## Create Location



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/storerocket/latest/actions/create-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "name": "Ava Chen",
  "addressLine1": "string",
  "city": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/storerocket/latest/actions/create-location', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "name": "Ava Chen",
    "addressLine1": "string",
    "city": "string"
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
      "address": "string",
      "addressLine1": "string",
      "addressLine2": "string",
      "callsToAction": [
        {}
      ],
      "city": "string",
      "country": "string",
      "coverImageUrl": "https://example.com",
      "displayAddress": "string",
      "email": "ava@example.com",
      "facebook": "string",
      "fields": [
        {}
      ],
      "filters": [
        {}
      ],
      "hours": {},
      "id": "string",
      "instagram": "string",
      "lat": 1,
      "lng": 1,
      "locationType": "string",
      "markerUrl": "https://example.com",
      "name": "Ava Chen",
      "phone": "string",
      "postcode": "string",
      "slug": "string",
      "state": "string",
      "twitter": "string",
      "url": "https://example.com",
      "visible": true,
      "yelp": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Location action reference](actions/create-location.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/storerocket/latest/actions/create-location).
