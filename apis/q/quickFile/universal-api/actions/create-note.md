# QuickFile: Create Note



```
POST https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/create-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/create-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "note": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/create-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "note": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `note` | string | yes | Note body to attach in QuickFile. |
| `postedBy` | string | no | Display name to attribute on the note. Default: `MindCloud`. |
| `clientId` | number | no | Client record to attach the note to. |
| `supplierId` | number | no | Supplier record to attach the note to. |
| `invoiceId` | number | no | Invoice record to attach the note to. |
| `purchaseId` | number | no | Purchase record to attach the note to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "noteCreated": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `noteCreated` | boolean | Whether the QuickFile note was created successfully. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /system/createnote` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-note.md) for the provider-specific parameters and requirements.

