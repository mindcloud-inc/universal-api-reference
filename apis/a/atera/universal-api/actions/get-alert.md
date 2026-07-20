# Atera: Get alert

Retrieves an alert from Atera by ID.

```
GET https://connect.mindcloud.co/v1/universal/atera/latest/actions/get-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atera/latest/actions/get-alert?connectionId=$CONNECTION_ID&alertId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "alertId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atera/latest/actions/get-alert?${params}`, {
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
| `alertId` | number | yes | System alert ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AdditionalInfo": "string",
      "AgentId": 1,
      "AlertCategoryID": "string",
      "AlertID": 1,
      "AlertMessage": "string",
      "Archived": true,
      "ArchivedDate": "string",
      "Code": 1,
      "Created": "string",
      "CustomerID": 1,
      "CustomerName": "Ava Chen",
      "DeviceGuid": "string",
      "DeviceName": "Ava Chen",
      "FolderID": 1,
      "MessageTemplate": "string",
      "PollingCyclesCount": 1,
      "Severity": "string",
      "SnoozedEndDate": "string",
      "Source": "string",
      "ThresholdValue1": "string",
      "ThresholdValue2": "string",
      "ThresholdValue3": "string",
      "ThresholdValue4": "string",
      "ThresholdValue5": "string",
      "TicketID": 1,
      "Title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AdditionalInfo` | string | Additional provider details. |
| `AgentId` | number | Associated agent ID. |
| `AlertCategoryID` | string | Alert category. |
| `AlertID` | number | Atera alert ID. |
| `AlertMessage` | string | Rendered alert message. |
| `Archived` | boolean | Whether the alert is archived. |
| `ArchivedDate` | string | Archived timestamp. |
| `Code` | number | Provider alert code. |
| `Created` | string | Alert creation timestamp. |
| `CustomerID` | number | Owning customer ID. |
| `CustomerName` | string | Owning customer name. |
| `DeviceGuid` | string | Associated device GUID. |
| `DeviceName` | string | Associated device name. |
| `FolderID` | number | Folder ID, when present. |
| `MessageTemplate` | string | Underlying message template. |
| `PollingCyclesCount` | number | Polling cycle count. |
| `Severity` | string | Alert severity. |
| `SnoozedEndDate` | string | Snooze expiry timestamp. |
| `Source` | string | Alert source. |
| `ThresholdValue1` | string | First threshold value. |
| `ThresholdValue2` | string | Second threshold value. |
| `ThresholdValue3` | string | Third threshold value. |
| `ThresholdValue4` | string | Fourth threshold value. |
| `ThresholdValue5` | string | Fifth threshold value. |
| `TicketID` | number | Linked ticket ID, when present. |
| `Title` | string | Alert title. |

## Native endpoint

Through the native Atera API, this operation is `GET /api/v3/alerts/:alertId` (base URL `https://app.atera.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-alert.md) for the provider-specific parameters and requirements.

