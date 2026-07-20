# Synchroteam: Get Equipment

Retrieves equipment from Synchroteam by supported identifier.

```
GET https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/get-equipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Synchroteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/get-equipment?connectionId=$CONNECTION_ID&identifierType=string&identifierValue=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifierType": "string",
  "identifierValue": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/get-equipment?${params}`, {
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
      "CustomerId": 1,
      "CustomerMyId": "string",
      "CustomerName": "Ava Chen",
      "Name": "Ava Chen",
      "publicLink": "https://example.com",
      "SiteName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CustomerId` | number |  |
| `CustomerMyId` | string |  |
| `CustomerName` | string |  |
| `Name` | string |  |
| `publicLink` | string |  |
| `SiteName` | string |  |

## Native endpoint

Through the native Synchroteam API, this operation is `GET /Api/v2/Equipment/Details` (base URL `https://ws.synchroteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-equipment.md) for the provider-specific parameters and requirements.

