# Synchroteam: Get Site

Retrieves a site from Synchroteam by supported identifier.

```
GET https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/get-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Synchroteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/get-site?connectionId=$CONNECTION_ID&identifierType=string&identifierValue=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifierType": "string",
  "identifierValue": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/get-site?${params}`, {
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
| `identifierType` | string | yes | Which identifier to use (for example: name, id, myId). |
| `identifierValue` | string | yes | The identifier value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Address": "string",
      "AddressComplement": "string",
      "ContactEmail": "ava@example.com",
      "CustomerId": 1,
      "CustomerMyId": "string",
      "CustomerName": "Ava Chen",
      "MyId": "string",
      "Name": "Ava Chen",
      "publicLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Address` | string |  |
| `AddressComplement` | string |  |
| `ContactEmail` | string |  |
| `CustomerId` | number |  |
| `CustomerMyId` | string |  |
| `CustomerName` | string |  |
| `MyId` | string |  |
| `Name` | string |  |
| `publicLink` | string |  |

## Native endpoint

Through the native Synchroteam API, this operation is `GET /Api/v2/Site/Details` (base URL `https://ws.synchroteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site.md) for the provider-specific parameters and requirements.

