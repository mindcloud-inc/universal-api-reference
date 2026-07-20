# Flatfile: Find And Replace Records

Finds and replaces matching record values in Flatfile.

```
PUT https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/find-and-replace-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flatfile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/find-and-replace-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fieldKey": "status",
  "sheetId": "us_sht_mindcloud_flatfile"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/find-and-replace-records', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fieldKey": "status",
    "sheetId": "us_sht_mindcloud_flatfile"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fieldKey` | string | yes | Field key to search and replace. Default: `status`. |
| `sheetId` | string | yes | Flatfile sheet identifier. Default: `us_sht_mindcloud_flatfile`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Find-and-replace result. |

## Native endpoint

Through the native Flatfile API, this operation is `PUT /sheets/:sheetId/find-replace` (base URL `https://api.x.flatfile.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-and-replace-records.md) for the provider-specific parameters and requirements.

