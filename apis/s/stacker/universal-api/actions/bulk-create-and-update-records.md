# Stacker: Bulk Create and Update Records

Creates or updates records in a Stacker object.

```
PUT https://connect.mindcloud.co/v1/universal/stacker/latest/actions/bulk-create-and-update-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stacker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stacker/latest/actions/bulk-create-and-update-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "objectSid": "string",
  "records[]": [
    {}
  ],
  "stackId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stacker/latest/actions/bulk-create-and-update-records', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "objectSid": "string",
    "records[]": [{}],
    "stackId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | Stacker account ID sent as the X-Account-Id header. |
| `objectSid` | string | yes | Object SID from the Stacker endpoint path. |
| `records[]` | array<object> | yes | Array of record objects using Stacker field API names. Include `_sid` to update an existing record. |
| `stackId` | string | yes | Stacker stack ID sent as the X-Stack-Id header. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": [
        "string"
      ],
      "formatting_errors": [
        {}
      ],
      "updated": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | array<string> | Record SIDs created by the bulk request. |
| `formatting_errors` | array<object> | Per-record formatting errors returned by Stacker when present. |
| `updated` | array<string> | Record SIDs updated by the bulk request. |

## Native endpoint

Through the native Stacker API, this operation is `POST /api/external/objects/:object_sid/bulk-records/` (base URL `https://api.go.stackerhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-create-and-update-records.md) for the provider-specific parameters and requirements.

