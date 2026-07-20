# MoySklad: Delete document position

Deletes a document position from MoySklad.

```
DELETE https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/delete-document-position
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoySklad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/delete-document-position?connectionId=$CONNECTION_ID&entityType=customerorder&id=28e45ad1-3d81-11f1-0a80-0b450021d671&positionId=89e05606-3ce8-11f1-0a80-161100021282" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entityType": "customerorder",
  "id": "28e45ad1-3d81-11f1-0a80-0b450021d671",
  "positionId": "89e05606-3ce8-11f1-0a80-161100021282"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/delete-document-position?${params}`, {
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
| `entityType` | string | yes | MoySklad document type. Default: `customerorder`. |
| `id` | string | yes | MoySklad document ID. Default: `28e45ad1-3d81-11f1-0a80-0b450021d671`. |
| `positionId` | string | yes | MoySklad position ID. Default: `89e05606-3ce8-11f1-0a80-161100021282`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "meta": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `meta` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native MoySklad API, this operation is `DELETE entity/:entityType/:id/positions/:positionId` (base URL `https://api.moysklad.ru/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-document-position.md) for the provider-specific parameters and requirements.

