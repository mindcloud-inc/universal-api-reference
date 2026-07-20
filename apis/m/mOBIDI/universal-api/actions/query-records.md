# MOBIDI: Query Records

Retrieves records from a MOBIDI query.

```
GET https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/query-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MOBIDI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/query-records?connectionId=$CONNECTION_ID&queryObject=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "queryObject": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/query-records?${params}`, {
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
| `queryObject` | string | yes | Serialized MobidiQuery payload. |

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

Through the native MOBIDI API, this operation is `POST /MobidiQueryManagerHandler` (base URL `https://servis2.dece.com.tr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-records.md) for the provider-specific parameters and requirements.

