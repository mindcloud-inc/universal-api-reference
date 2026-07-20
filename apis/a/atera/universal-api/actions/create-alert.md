# Atera: Create alert

Creates an alert in Atera.

```
POST https://connect.mindcloud.co/v1/universal/atera/latest/actions/create-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/atera/latest/actions/create-alert" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "deviceGuid": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atera/latest/actions/create-alert', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "deviceGuid": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `additionalInfo` | string | no | Additional alert details. |
| `alertCategoryId` | string | no | Alert category. |
| `code` | number | no | Alert code. |
| `customerId` | number | yes | Customer ID for the alert. |
| `deviceGuid` | string | yes | Global unique device identifier. |
| `folderId` | number | no | Folder ID. |
| `messageTemplate` | string | no | Alert message template. |
| `severity` | string | no | Alert severity. |
| `snoozedEndDate` | string | no | UTC snooze end timestamp. |
| `thresholdValue1` | string | no | First threshold value. |
| `thresholdValue2` | string | no | Second threshold value. |
| `thresholdValue3` | string | no | Third threshold value. |
| `thresholdValue4` | string | no | Fourth threshold value. |
| `thresholdValue5` | string | no | Fifth threshold value. |
| `ticketId` | number | no | Related ticket ID. |
| `title` | string | yes | Alert title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ActionID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ActionID` | string | Inferred Atera write-action success identifier. Validate against a live device GUID before relying on this shape in production workflows. |

## Native endpoint

Through the native Atera API, this operation is `POST /api/v3/alerts` (base URL `https://app.atera.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-alert.md) for the provider-specific parameters and requirements.

