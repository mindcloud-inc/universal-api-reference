# ClassMarker: Remove Access Codes



```
PUT https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/remove-access-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClassMarker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/remove-access-codes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accessListId": 1,
  "accessCodes[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/remove-access-codes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accessListId": 1,
    "accessCodes[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accessListId` | number | yes | Numeric ClassMarker access list ID. |
| `accessCodes[]` | array<string> | yes | Access codes to remove from the access list. ClassMarker allows up to 100 codes per request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessLists": {
        "accessList": {
          "accessListId": 1,
          "accessListName": "Ava Chen",
          "numCodesDeleted": 1,
          "numCodesTotal": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessLists.accessList.accessListId` | number |  |
| `accessLists.accessList.accessListName` | string |  |
| `accessLists.accessList.numCodesDeleted` | number |  |
| `accessLists.accessList.numCodesTotal` | number |  |

## Native endpoint

Through the native ClassMarker API, this operation is `DELETE /v1/accesslists/{access_list_id}.json` (base URL `https://api.classmarker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-access-codes.md) for the provider-specific parameters and requirements.

