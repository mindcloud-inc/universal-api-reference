# Zoho ZeptoMail: List Exports

Retrieves log exports from Zoho ZeptoMail.

```
GET https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/list-exports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho ZeptoMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/list-exports?connectionId=$CONNECTION_ID&exportType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "exportType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/list-exports?${params}`, {
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
| `exportType` | string | yes | Export category to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "created_time": "2026-05-07T12:00:00.000Z",
          "export_id": "string",
          "export_type": "string",
          "modified_time": "2026-05-07T12:00:00.000Z",
          "status": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].created_time` | date |  |
| `data[].export_id` | string |  |
| `data[].export_type` | string |  |
| `data[].modified_time` | date |  |
| `data[].status` | string |  |

## Native endpoint

Through the native Zoho ZeptoMail API, this operation is `GET :exportType/exports` (base URL `https://api.zeptomail.com/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-exports.md) for the provider-specific parameters and requirements.

