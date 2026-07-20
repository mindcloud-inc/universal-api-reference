# ServiceTrade Universal API Examples

These examples use the MindCloud API key and ServiceTrade connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get OAuth2 Userinfo



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/get-oauth2-userinfo?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/get-oauth2-userinfo?${params}`, {
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
      "account": {
        "id": 1,
        "name": "Ava Chen",
        "uri": "string"
      },
      "clientId": "string",
      "company": {
        "id": 1,
        "name": "Ava Chen",
        "status": "string",
        "uri": "string"
      },
      "environment": "string",
      "isDemo": true,
      "name": "Ava Chen",
      "status": "string",
      "timezone": "string",
      "type": "string",
      "uri": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

See the full [Get OAuth2 Userinfo action reference](actions/get-oauth2-userinfo.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/serviceTrade/latest/actions/get-oauth2-userinfo).

## Create Asset

Creates a new asset in ServiceTrade.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/create-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "locationId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/create-asset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "locationId": 1
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
      "assetDefinition": {
        "display": "string",
        "id": 1,
        "type": "string"
      },
      "created": 1,
      "display": "string",
      "externalIds": {
        "quickbooks": "string"
      },
      "hasActiveTaskList": true,
      "id": 1,
      "isAbstractGroup": true,
      "legacyId": "string",
      "location": {
        "address": {
          "city": "string",
          "state": "string"
        },
        "id": 1,
        "name": "Ava Chen",
        "refNumber": "string",
        "status": "string"
      },
      "name": "Ava Chen",
      "orderIndex": 1,
      "parent": {
        "id": 1,
        "name": "Ava Chen",
        "type": "string"
      },
      "serviceLine": {
        "abbr": "string",
        "id": 1,
        "name": "Ava Chen",
        "trade": "string"
      },
      "status": "string",
      "type": "string",
      "updated": 1,
      "uri": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Asset action reference](actions/create-asset.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/serviceTrade/latest/actions/create-asset).
