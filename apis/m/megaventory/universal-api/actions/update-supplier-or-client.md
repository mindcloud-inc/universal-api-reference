# Megaventory: Update Supplier or Client

Updates a supplier or client in Megaventory using a record action.

```
PUT https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/update-supplier-or-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Megaventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/update-supplier-or-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mvSupplierClient": {},
  "mvRecordAction": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/update-supplier-or-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mvSupplierClient": {},
    "mvRecordAction": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mvSupplierClient` | object | yes | Supplier or client payload to insert, update, or delete. |
| `mvRecordAction` | string | yes | Megaventory record action such as Insert, Update, or Delete. |
| `mvGrantPermissionsToAllUsers` | boolean | no | Grant created record permissions to all users. |
| `mvInsertUpdateDeleteSourceApplication` | string | no | Source application label Megaventory should store for the change. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entityID": 1,
      "mvSupplierClient": {},
      "ResponseStatus": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entityID` | number |  |
| `mvSupplierClient` | object |  |
| `ResponseStatus` | object |  |

## Native endpoint

Through the native Megaventory API, this operation is `POST /json/reply/SupplierClientUpdate` (base URL `https://api.megaventory.com/v2017a`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-supplier-or-client.md) for the provider-specific parameters and requirements.

