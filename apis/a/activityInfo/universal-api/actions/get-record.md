# ActivityInfo: Get Record

Retrieves a record from an ActivityInfo form.

```
GET https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivityInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-record?connectionId=$CONNECTION_ID&formId=string&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-record?${params}`, {
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
| `formId` | string | yes | ActivityInfo form ID. |
| `recordId` | string | yes | ActivityInfo record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": {},
      "formId": "string",
      "lastEditTime": 1,
      "parentRecordId": "string",
      "recordId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields` | object | Record field values keyed by field ID. |
| `formId` | string | Form ID. |
| `lastEditTime` | number | Last edit time. |
| `parentRecordId` | string | Parent record ID, when present. |
| `recordId` | string | Record ID. |

## Native endpoint

Through the native ActivityInfo API, this operation is `GET /resources/form/:formId/record/:recordId` (base URL `https://www.activityinfo.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-record.md) for the provider-specific parameters and requirements.

