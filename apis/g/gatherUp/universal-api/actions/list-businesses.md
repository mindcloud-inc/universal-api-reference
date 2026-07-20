# GatherUp: List Businesses

Retrieves a list of businesses from GatherUp.

```
GET https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-businesses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-businesses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-businesses?${params}`, {
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
| `includeDeletedBusinesses` | number | no | Set to 0 if you want to hide deleted businesses, default value is 1. Default: `1`. |
| `page` | number | no | Page number, if not specified then page = 1 Default: `1`. |
| `limit` | number | no | Number of items per page, if not specified then limit = 100 Default: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessCity": "string",
      "businessCountry": "string",
      "businessDeleted": 1,
      "businessId": 1,
      "businessName": "Ava Chen",
      "businessOrganisationType": "string",
      "businessPackage": "string",
      "businessPhone": "string",
      "businessState": "string",
      "businessStreetAddress": "string",
      "businessWebsiteURL": "https://example.com",
      "businessZip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessCity` | string |  |
| `businessCountry` | string |  |
| `businessDeleted` | number |  |
| `businessId` | number |  |
| `businessName` | string |  |
| `businessOrganisationType` | string |  |
| `businessPackage` | string |  |
| `businessPhone` | string |  |
| `businessState` | string |  |
| `businessStreetAddress` | string |  |
| `businessWebsiteURL` | string |  |
| `businessZip` | string |  |

## Native endpoint

Through the native GatherUp API, this operation is `POST /businesses/get` (base URL `https://app.gatherup.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-businesses.md) for the provider-specific parameters and requirements.

