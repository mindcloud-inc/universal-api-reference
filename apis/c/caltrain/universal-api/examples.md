# Caltrain Universal API Examples

These examples use the MindCloud API key and Caltrain connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Stop Alerts

Retrieves alerts for a Caltrain stop.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/get-stop-alerts?connectionId=$CONNECTION_ID&stopId=22nd_street" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stopId": "22nd_street"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/get-stop-alerts?${params}`, {
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
      "meta": {
        "stop": {
          "childStopIds": {
            "7075": "string",
            "7076": "string",
            "11226": "string",
            "11227": "string"
          },
          "fieldAgencyId": [
            {
              "value": "string"
            }
          ],
          "fieldAmenitiesBenefits": [
            {
              "targetId": "string",
              "targetRevisionId": "string"
            }
          ],
          "fieldBody": [
            {
              "targetId": "string",
              "targetRevisionId": "string"
            }
          ],
          "fieldImage": [
            {
              "targetId": "string"
            }
          ],
          "fieldLocation": [
            {
              "bottom": 1,
              "geohash": "string",
              "geoType": "string",
              "lat": 1,
              "latlon": "string",
              "left": 1,
              "lon": 1,
              "right": 1,
              "top": 1,
              "value": "string"
            }
          ],
          "fieldLocationType": [
            {
              "value": "string"
            }
          ],
          "fieldServicedRoutes": [
            {
              "targetId": "string"
            }
          ],
          "fieldStopId": [
            {
              "value": "string"
            }
          ],
          "fieldTransitConnections": [
            {
              "targetId": "string",
              "targetRevisionId": "string"
            }
          ],
          "nid": [
            {
              "value": "string"
            }
          ],
          "path": [
            {
              "alias": "string",
              "langcode": "string",
              "pid": "string"
            }
          ],
          "title": [
            {
              "value": "string"
            }
          ],
          "type": [
            {
              "targetId": "string"
            }
          ]
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Stop Alerts action reference](actions/get-stop-alerts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/caltrain/latest/actions/get-stop-alerts).
