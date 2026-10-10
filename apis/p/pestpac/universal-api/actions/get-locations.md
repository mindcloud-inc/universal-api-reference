# PestPac: Get Locations



```
GET https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/get-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PestPac `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/get-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/get-locations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ids` | string | no |  |
| `q` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountType": "string",
      "active": true,
      "address": "string",
      "address2": "string",
      "alternatePhone": "string",
      "billToID": 1,
      "branch": "string",
      "branchID": 1,
      "city": "string",
      "company": "string",
      "doNotGeocode": true,
      "email": "ava@example.com",
      "firstName": "Ava",
      "internalIdentifier": "string",
      "lastName": "Chen",
      "latitude": 1,
      "locationCode": "string",
      "locationID": 1,
      "longitude": 1,
      "mobilePhone": "string",
      "phone": "string",
      "showOnLogBook": true,
      "smsMarketing": true,
      "source": "string",
      "state": "string",
      "subdivision": "string",
      "type": "string",
      "userDefinedFields": [
        {
          "caption": "string",
          "description": "string",
          "fieldNum": 1,
          "show": true,
          "tableName": "Ava Chen",
          "type": "string",
          "value": "string"
        }
      ],
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountType` | string |  |
| `active` | boolean |  |
| `address` | string |  |
| `address2` | string |  |
| `alternatePhone` | string |  |
| `billToID` | number |  |
| `branch` | string |  |
| `branchID` | number |  |
| `city` | string |  |
| `company` | string |  |
| `doNotGeocode` | boolean |  |
| `email` | string |  |
| `firstName` | string |  |
| `internalIdentifier` | string |  |
| `lastName` | string |  |
| `latitude` | number |  |
| `locationCode` | string |  |
| `locationID` | number |  |
| `longitude` | number |  |
| `mobilePhone` | string |  |
| `phone` | string |  |
| `showOnLogBook` | boolean |  |
| `smsMarketing` | boolean |  |
| `source` | string |  |
| `state` | string |  |
| `subdivision` | string |  |
| `type` | string |  |
| `userDefinedFields[].caption` | string |  |
| `userDefinedFields[].description` | string |  |
| `userDefinedFields[].fieldNum` | number |  |
| `userDefinedFields[].show` | boolean |  |
| `userDefinedFields[].tableName` | string |  |
| `userDefinedFields[].type` | string |  |
| `userDefinedFields[].value` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native PestPac API, this operation is `GET Locations` (base URL `https://api.workwave.com/pestpac/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-locations.md) for the provider-specific parameters and requirements.

