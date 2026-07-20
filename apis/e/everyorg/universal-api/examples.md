# Every.org Universal API Examples

These examples use the MindCloud API key and Every.org connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Nonprofit

Retrieves details about a nonprofit from Every.org.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/get-nonprofit?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/get-nonprofit?${params}`, {
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
      "nonprofit": {
        "coverImageCloudinaryId": "string",
        "coverImageUrl": "https://example.com",
        "description": "string",
        "descriptionLong": "string",
        "disbursementType": "string",
        "donationsEnabled": true,
        "ein": "string",
        "hasAdmin": true,
        "id": "string",
        "locationAddress": "string",
        "locationLatLng": {
          "coordinates": [
            1
          ],
          "type": "string"
        },
        "logoCloudinaryId": "string",
        "logoUrl": "https://example.com",
        "name": "Ava Chen",
        "nteeCode": "string",
        "nteeCodeMeaning": {
          "decileCode": "string",
          "decileMeaning": "string",
          "majorCode": "string",
          "majorMeaning": "string"
        },
        "primarySlug": "string",
        "profileUrl": "https://example.com",
        "websiteUrl": "https://example.com"
      },
      "nonprofitTags": [
        {
          "causeCategory": "string",
          "id": "string",
          "tagImageCloudinaryId": "string",
          "tagImageUrl": "https://example.com",
          "tagName": "Ava Chen",
          "tagUrl": "https://example.com",
          "title": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Nonprofit action reference](actions/get-nonprofit.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/everyorg/latest/actions/get-nonprofit).

## Create Fundraiser

Creates a new fundraiser in Every.org.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/create-fundraiser" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "nonprofitId": "string",
  "title": "string",
  "description": "string",
  "goal": 1,
  "raisedOffline": 1,
  "startDate": "string",
  "endDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/create-fundraiser', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "nonprofitId": "string",
    "title": "string",
    "description": "string",
    "goal": 1,
    "raisedOffline": 1,
    "startDate": "string",
    "endDate": "string"
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
      "fundraiser": {
        "active": true,
        "description": "string",
        "goalAmount": "string",
        "goalCurrency": "string",
        "id": "string",
        "nonprofitId": "string",
        "slug": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Fundraiser action reference](actions/create-fundraiser.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/everyorg/latest/actions/create-fundraiser).
