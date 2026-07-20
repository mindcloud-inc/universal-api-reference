# DitLead: Get List



```
GET https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/get-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DitLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/get-list?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/get-list?${params}`, {
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
| `listId` | string | yes | Public ID of the list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createdAt": "string",
        "listName": "Ava Chen",
        "listType": "string",
        "publicId": "string",
        "status": {},
        "verifyList": true
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.createdAt` | string |  |
| `data.listName` | string |  |
| `data.listType` | string |  |
| `data.publicId` | string |  |
| `data.status` | object |  |
| `data.verifyList` | boolean |  |
| `success` | boolean |  |

## Native endpoint

Through the native DitLead API, this operation is `GET /v1/list/{listId}` (base URL `https://api.ditlead.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list.md) for the provider-specific parameters and requirements.

