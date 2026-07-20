# Melo Universal API Examples

These examples use the MindCloud API key and Melo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Departments



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/melo/latest/actions/list-departments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/melo/latest/actions/list-departments?${params}`, {
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
      "chefLieu": "string",
      "departmentCode": "string",
      "name": "Ava Chen",
      "nameClean": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Departments action reference](actions/list-departments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/melo/latest/actions/list-departments).

## Create Search

Creates a new search in Melo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/melo/latest/actions/create-search" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "transactionType": "1",
  "propertyTypes[]": "0,1",
  "includedDepartments[]": "[/departments/77]",
  "budgetMax": "350000"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/melo/latest/actions/create-search', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "transactionType": "1",
    "propertyTypes[]": "0,1",
    "includedDepartments[]": "[/departments/77]",
    "budgetMax": "350000"
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
      "advertPriceMax": {},
      "advertPriceMin": {},
      "bedroomMin": {},
      "budgetMax": 1,
      "budgetMin": {},
      "createdAt": "string",
      "endpointRecipient": {},
      "eventEndpoint": {},
      "furnished": {},
      "geoShapes": {},
      "hidePropertyContact": true,
      "includedDepartments": [
        {
          "chefLieu": "string",
          "departmentCode": "string",
          "name": "Ava Chen",
          "nameClean": "Ava Chen"
        }
      ],
      "initiatedFromDashboard": true,
      "landSurfaceMax": {},
      "landSurfaceMin": {},
      "lastAlertAt": {},
      "lat": {},
      "lon": {},
      "notificationEnabled": true,
      "notificationRecipient": {},
      "pricePerMeterMax": {},
      "pricePerMeterMin": {},
      "propertyTypes": [
        1
      ],
      "radius": {},
      "roomMin": {},
      "surfaceMax": {},
      "surfaceMin": {},
      "title": "string",
      "token": "string",
      "transactionType": 1,
      "updatedAt": "string",
      "user": "string",
      "withCoherentPrice": true,
      "withVirtualTour": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Search action reference](actions/create-search.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/melo/latest/actions/create-search).
