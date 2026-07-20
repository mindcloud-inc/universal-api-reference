# PeakIDX Universal API Examples

These examples use the MindCloud API key and PeakIDX connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Search Criteria

Retrieves configured search criteria from PeakIDX.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peakIDX/latest/actions/get-search-criteria?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peakIDX/latest/actions/get-search-criteria?${params}`, {
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
      "acreage": [
        [
          {}
        ]
      ],
      "bathrooms": [
        [
          {}
        ]
      ],
      "bedrooms": [
        [
          {}
        ]
      ],
      "listStatus": [
        [
          {}
        ]
      ],
      "price": [
        [
          {}
        ]
      ],
      "sort": [
        [
          {}
        ]
      ],
      "sqft": [
        [
          {}
        ]
      ],
      "status": [
        [
          {}
        ]
      ],
      "type": [
        [
          {}
        ]
      ],
      "yearBuilt": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Search Criteria action reference](actions/get-search-criteria.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/peakIDX/latest/actions/get-search-criteria).

## Create Or Update Lead

Creates or updates a lead in PeakIDX.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/peakIDX/latest/actions/create-or-update-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/peakIDX/latest/actions/create-or-update-lead', {
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Or Update Lead action reference](actions/create-or-update-lead.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/peakIDX/latest/actions/create-or-update-lead).
