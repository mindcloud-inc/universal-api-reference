# OneSignal: Export Audience Activity CSV

Exports audience activity as CSV from OneSignal.

```
GET https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/export-audience-activity-csv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/export-audience-activity-csv?connectionId=$CONNECTION_ID&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/export-audience-activity-csv?${params}`, {
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
| `messageId` | string | yes | The identifier of the message in UUID v4 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "csvFileUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `csvFileUrl` | string | The download URL for the generated audience activity CSV export. |

## Native endpoint

Through the native OneSignal API, this operation is `POST /notifications/:message_id/export_events` (base URL `https://api.onesignal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-audience-activity-csv.md) for the provider-specific parameters and requirements.

