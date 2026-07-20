# Zoho Creator: Publish Add Records

Creates new records through a Zoho Creator publish form.

```
POST https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/publish-add-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Creator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/publish-add-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountOwnerName": "Ava Chen",
  "appLinkName": "https://example.com",
  "formLinkName": "https://example.com",
  "privateLink": "https://example.com",
  "data[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/publish-add-records', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountOwnerName": "Ava Chen",
    "appLinkName": "https://example.com",
    "formLinkName": "https://example.com",
    "privateLink": "https://example.com",
    "data[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountOwnerName` | string | yes | Zoho Creator account owner name. |
| `appLinkName` | string | yes | Zoho Creator app link name. |
| `formLinkName` | string | yes | Zoho Creator form link name. |
| `privateLink` | string | yes | Zoho Creator publish API private link token. |
| `result` | object | no | Response result preferences. |
| `data[]` | array<object> | yes | Array of record objects to create through the publish API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "result": [
        {
          "code": 1,
          "data": {
            "id": "string"
          },
          "message": "string",
          "tasks": {}
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
| `code` | number | Zoho Creator response code. |
| `result` | array<object> | Per-record publish add results returned by Zoho Creator. |
| `result[].code` | number | Zoho Creator status code for the individual published record create attempt. |
| `result[].data` | object | Created record values returned for the individual published record create attempt. |
| `result[].data.id` | string | Identifier of the created published record. |
| `result[].message` | string | Status message for the individual published record create attempt. |
| `result[].tasks` | object | Optional task directives returned by Zoho Creator for the published record create attempt. |

## Native endpoint

Through the native Zoho Creator API, this operation is `POST /publish/:account_owner_name/:app_link_name/form/:form_link_name` (base URL `https://www.zohoapis.com/creator/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-add-records.md) for the provider-specific parameters and requirements.

