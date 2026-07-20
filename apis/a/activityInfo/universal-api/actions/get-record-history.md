# ActivityInfo: Get Record History

Retrieves a record's history from ActivityInfo.

```
GET https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-record-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivityInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-record-history?connectionId=$CONNECTION_ID&formId=string&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-record-history?${params}`, {
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
      "entries": [
        {}
      ],
      "formId": "string",
      "recordId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entries` | array<object> | Record history entries. |
| `formId` | string | Form ID. |
| `recordId` | string | Record ID. |

## Native endpoint

Through the native ActivityInfo API, this operation is `GET /resources/form/:formId/record/:recordId/history` (base URL `https://www.activityinfo.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-record-history.md) for the provider-specific parameters and requirements.

