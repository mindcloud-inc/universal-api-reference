# MOBIDI: Get Record Change Log

Retrieves a record change log from MOBIDI.

```
GET https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/get-record-change-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MOBIDI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/get-record-change-log?connectionId=$CONNECTION_ID&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/get-record-change-log?${params}`, {
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
| `recordId` | string | yes | MOBIDI record identifier. |
| `updateUserNames` | boolean | no | Whether to resolve user display names in the log. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BeforeObject": {},
      "ChangeTime": {},
      "ChangeType": 1,
      "ChangeTypeName": "Ava Chen",
      "CurrentObject": {},
      "ExtraInfo": "string",
      "LogTempUser": "string",
      "TypeInfo": "string",
      "UniqueID": "string",
      "User": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BeforeObject` | object | Record state before the change. |
| `ChangeTime` | object | Timestamp wrapper for the change. |
| `ChangeType` | number | Numeric change type code. |
| `ChangeTypeName` | string | Change type label. |
| `CurrentObject` | object | Record state after the change. |
| `ExtraInfo` | string | Provider extra info payload. |
| `LogTempUser` | string | Temporary user label captured in the log. |
| `TypeInfo` | string | Provider change object type. |
| `UniqueID` | string | Affected record identifier. |
| `User` | string | User who made the change. |

## Native endpoint

Through the native MOBIDI API, this operation is `POST /MobidiQueryManagerHandler` (base URL `https://servis2.dece.com.tr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-record-change-log.md) for the provider-specific parameters and requirements.

