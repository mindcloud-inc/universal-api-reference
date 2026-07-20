# DatoCMS Universal API Examples

These examples use the MindCloud API key and DatoCMS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Site



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-site?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-site?${params}`, {
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
        "assetsCdnDefaultSettings": {
          "image": {
            "auto": [
              "string"
            ]
          },
          "video": {
            "disableServingRawVideos": true
          }
        },
        "domain": "string",
        "favicon": "string",
        "forceUseOfSandboxEnvironments": true,
        "globalSeo": "string",
        "googleMapsApiToken": "string",
        "imgixHost": "string",
        "internalDomain": "string",
        "ipTrackingEnabled": true,
        "lastDataChangeAt": "2026-05-07T12:00:00.000Z",
        "locales": [
          "string"
        ],
        "name": "Ava Chen",
        "noIndex": true,
        "require2fa": true,
        "theme": {
          "accentColor": {
            "alpha": 1,
            "blue": 1,
            "green": 1,
            "red": 1
          },
          "darkColor": {
            "alpha": 1,
            "blue": 1,
            "green": 1,
            "red": 1
          },
          "hue": 1,
          "lightColor": {
            "alpha": 1,
            "blue": 1,
            "green": 1,
            "red": 1
          },
          "logo": "string",
          "primaryColor": {
            "alpha": 1,
            "blue": 1,
            "green": 1,
            "red": 1
          },
          "type": "string"
        },
        "timezone": "string"
      },
      "id": "string",
      "meta": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "customUploadStorageSettings": true,
        "draftModeDefault": true,
        "improvedBooleanFields": true,
        "improvedExposureOfInlineBlocksInCda": true,
        "improvedGqlMultilocaleFields": true,
        "improvedGqlVisibilityControl": true,
        "improvedHexManagement": true,
        "improvedItemsListing": true,
        "improvedTimezoneManagement": true,
        "improvedValidationAtPublishing": true,
        "millisecondsInDatetime": true
      },
      "relationships": {
        "account": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "itemTypes": {
          "data": [
            {
              "id": "string",
              "type": "string"
            }
          ]
        },
        "owner": {
          "data": {
            "id": "string",
            "type": "string"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Site action reference](actions/get-site.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/datoCMS/latest/actions/get-site).

## Create Draft Record



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/create-draft-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemTypeId": "Ey1hk04gQ9ib4oyfQuFK5A",
  "attributes": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/create-draft-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemTypeId": "Ey1hk04gQ9ib4oyfQuFK5A",
    "attributes": "[object Object]"
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
      "attributes": {},
      "id": "string",
      "meta": {},
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Draft Record action reference](actions/create-draft-record.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/datoCMS/latest/actions/create-draft-record).
