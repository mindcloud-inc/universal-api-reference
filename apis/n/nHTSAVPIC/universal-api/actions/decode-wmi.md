# NHTSA vPIC: Decode WMI

Decodes a WMI with NHTSA vPIC.

```
GET https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/decode-wmi
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NHTSA vPIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/decode-wmi?connectionId=$CONNECTION_ID&wmi=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "wmi": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/decode-wmi?${params}`, {
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
| `wmi` | string | yes | A 3-character WMI code or 6-character WMI segment to decode. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commonName": "Ava Chen",
      "createdOn": "string",
      "dateAvailableToPublic": "string",
      "make": "string",
      "manufacturerName": "Ava Chen",
      "parentCompanyName": "Ava Chen",
      "updatedOn": "string",
      "url": "https://example.com",
      "vehicleType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commonName` | string |  |
| `createdOn` | string |  |
| `dateAvailableToPublic` | string |  |
| `make` | string |  |
| `manufacturerName` | string |  |
| `parentCompanyName` | string |  |
| `updatedOn` | string |  |
| `url` | string |  |
| `vehicleType` | string |  |

## Native endpoint

Through the native NHTSA vPIC API, this operation is `GET vehicles/DecodeWMI/:wmi` (base URL `https://vpic.nhtsa.dot.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/decode-wmi.md) for the provider-specific parameters and requirements.

