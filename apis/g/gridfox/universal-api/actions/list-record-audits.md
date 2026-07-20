# Gridfox: List Record Audits

Retrieves audit entries for a Gridfox record.

```
GET https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/list-record-audits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gridfox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/list-record-audits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/list-record-audits?${params}`, {
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
| `referenceFieldValue` | string | no | Record reference field value from the path parameter. |
| `tableName` | string | no | Gridfox table name from the path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiIntegrationName": "Ava Chen",
      "comment": "string",
      "fieldName": "Ava Chen",
      "fieldType": "string",
      "isNewRecord": true,
      "recordTemplateName": "Ava Chen",
      "referenceFieldValue": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "userId": 1,
      "userName": "Ava Chen",
      "valueFrom": "string",
      "valueTo": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiIntegrationName` | string | Name of the API integration that made the change. |
| `comment` | string | Optional comment attached to the audit event. |
| `fieldName` | string | Field changed in the audit event. |
| `fieldType` | string | Gridfox field type. |
| `isNewRecord` | boolean | Whether the event corresponds to record creation. |
| `recordTemplateName` | string | Template name associated with the record. |
| `referenceFieldValue` | string | Record reference value. |
| `timestamp` | date | Timestamp of the audit event. |
| `userId` | number | Identifier of the user who made the change. |
| `userName` | string | Name of the user who made the change. |
| `valueFrom` | string | Previous field value. |
| `valueTo` | string | New field value. |

## Native endpoint

Through the native Gridfox API, this operation is `GET /data/:tableName/:referenceFieldValue/audit` (base URL `https://api.gridfox.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-record-audits.md) for the provider-specific parameters and requirements.

