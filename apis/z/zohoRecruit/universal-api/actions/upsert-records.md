# Zoho Recruit: Upsert Records

Inserts or updates records in a Zoho Recruit module.

```
POST https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/upsert-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Recruit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/upsert-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "moduleApiName": "Ava Chen",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/upsert-records', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "moduleApiName": "Ava Chen",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `moduleApiName` | string | yes | The Zoho Recruit module API name where the records should be upserted. |
| `data` | list<object> | yes | An array of record objects to upsert. |
| `duplicateCheckFields` | list<string> | no | Field API names to use for duplicate matching during upsert. |
| `trigger` | list<string> | no | Automation triggers to run after the upsert. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | array<object> |  |
| `data[].action` | string |  |
| `data[].code` | string |  |
| `data[].details` | object |  |
| `data[].details.createdBy` | object |  |
| `data[].details.createdBy.id` | string |  |
| `data[].details.createdBy.name` | string |  |
| `data[].details.createdTime` | string |  |
| `data[].details.id` | string |  |
| `data[].details.modifiedBy` | object |  |
| `data[].details.modifiedBy.id` | string |  |
| `data[].details.modifiedBy.name` | string |  |
| `data[].details.modifiedTime` | string |  |
| `data[].duplicateField` | object |  |
| `data[].message` | string |  |
| `data[].status` | string |  |

## Native endpoint

Through the native Zoho Recruit API, this operation is `POST /:moduleApiName/upsert` (base URL `https://recruit.zoho.com/recruit/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-records.md) for the provider-specific parameters and requirements.

