# Plasmic: Publish Item

Publishes an item in Plasmic CMS.

```
PUT https://connect.mindcloud.co/v1/universal/plasmic/latest/actions/publish-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Plasmic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/plasmic/latest/actions/publish-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "rowId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/plasmic/latest/actions/publish-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "rowId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `rowId` | string | yes | The Plasmic row identifier to publish. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "data": {},
      "draftData": {},
      "id": "string",
      "identifier": "string",
      "tableId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the row was created. |
| `data` | object | The published row data. |
| `draftData` | object | The draft row data, null after publish. |
| `id` | string | The row ID. |
| `identifier` | string | The row identifier. |
| `tableId` | string | The table ID. |
| `updatedAt` | date | When the row was last updated. |

## Native endpoint

Through the native Plasmic API, this operation is `POST /rows/:rowId/publish` (base URL `https://data.plasmic.app/api/v1/cms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-item.md) for the provider-specific parameters and requirements.

