# MOBIDI: Create Or Update Record

Creates or updates a record in MOBIDI.

```
POST https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/create-or-update-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MOBIDI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/create-or-update-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entry": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/create-or-update-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entry": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entry` | string | yes | Serialized MobidiEntry payload from the official EditMobidiEntry method. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `optionCheck` | boolean | no | Optional MOBIDI validation flag. Default: `false`. |
| `forOnlyAttachmentDelete` | boolean | no | Optional attachment-delete-only mode flag. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AlternateId": "string",
      "annotations": [
        {}
      ],
      "attachments": [
        {}
      ],
      "attributes": [
        {}
      ],
      "Info": "string",
      "IsReadonlyRecord": true,
      "points": {},
      "record": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AlternateId` | string | Optional alternate record identifier. |
| `annotations` | array<object> | Annotations for the record. |
| `attachments` | array<object> | Attachment list for the record. |
| `attributes` | array<object> | Attribute list for the record. |
| `Info` | string | Optional provider info message. |
| `IsReadonlyRecord` | boolean | Whether the returned record is read-only. |
| `points` | object | Optional point/geospatial payload. |
| `record` | object | Core MOBIDI record payload. |

## Native endpoint

Through the native MOBIDI API, this operation is `POST /MobidiQueryManagerHandler` (base URL `https://servis2.dece.com.tr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-record.md) for the provider-specific parameters and requirements.

