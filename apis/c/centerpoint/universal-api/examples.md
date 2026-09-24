# Centerpoint Universal API Examples

These examples use the MindCloud API key and Centerpoint connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Properties



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-properties?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-properties?${params}`, {
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
      "attributes": {
        "accountId": 1,
        "closeRate": {},
        "combinedMeasurement": "string",
        "companyId": 1,
        "county": "string",
        "createdAt": "string",
        "custom": {
          "kkclevel": {},
          "primaryonsitecontact": {},
          "roofaccess": {},
          "stagingandparkinglocation": {}
        },
        "customWithLabels": {
          "maintenancePlanLevel": {},
          "primaryOnsiteContact": {},
          "roofAccess": {},
          "stagingAndParkingLocation": {}
        },
        "deletedAt": {},
        "externalId": "string",
        "importId": {},
        "isVisible": true,
        "latitude": 1,
        "locality": "string",
        "locationId": 1,
        "longitude": 1,
        "managerId": {},
        "name": "Ava Chen",
        "postalCode": "string",
        "primaryBuildingId": 1,
        "primaryContractorId": {},
        "recentActivity": "string",
        "region": "string",
        "squares": 1,
        "streetAddress": "string",
        "subpremise": {},
        "timezone": "string",
        "updatedAt": "string",
        "uuid": "string",
        "weightedAverageScore": {}
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Properties action reference](actions/list-properties.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/centerpoint/latest/actions/list-properties).

## Create Company



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "type": "string",
  "salesStatus": "string",
  "timeZone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "type": "string",
    "salesStatus": "string",
    "timeZone": "string"
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

See the full [Create Company action reference](actions/create-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/centerpoint/latest/actions/create-company).
