# ServiceTitan: Update Technician



```
PUT https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-technician
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-technician" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-technician', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customFields[].typeId` | number | no |  |
| `id` | number | yes | ServiceTitan technician ID to update. |
| `customFields[].name` | string | no |  |
| `name` | string | no | Technician name. |
| `phoneNumber` | string | no | Technician phone number. |
| `email` | string | no | Technician email address. |
| `login` | string | no | Login username. |
| `businessUnitId` | number | no | Business unit ID. |
| `roleId` | number | no | User role ID. |
| `positions[]` | array<string> | no | Company positions. Allowed values: Installer, Service, Sales, Maintenance, Helper, InstallProductionManager, ServiceManager, SalesManager, PartRunner, DummyTech. |
| `licenseType` | list<string> | no | Technician license type: NonManagedTech, ManagedTech, or ManagedInstaller. One of: `ManagedInstaller`, `ManagedTech`, `NonManagedTech`. |
| `customFields[].value` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mainZoneId` | number | no | Main technician zone ID. |
| `zoneIds[]` | array<number> | no | All technician zone IDs. Sending this field replaces the existing zone list. |
| `projectLabelIds[]` | array<number> | no | Project label IDs. Sending this field replaces the existing list; it requires the Budget vs Actual feature flag. |
| `aadUserId` | string | no | Azure Active Directory user ID. |
| `team` | string | no | Team name. |
| `dailyGoal` | number | no | Daily revenue goal. |
| `burdenRate` | number | no | Hourly burden rate. |
| `bio` | string | no | Technician biography; ServiceTitan accepts HTML. |
| `memo` | string | no | Technician memo; ServiceTitan accepts HTML. |
| `jobFilter` | list<string> | no | Upcoming appointment visibility setting. One of: `AllScheduledDispatchedWorking`, `AllScheduledDispatchedWorkingFiveDays`, `AllScheduledDispatchedWorkingToday`, `AllScheduledDispatchedWorkingTodayTomorrow`, `DispatchedWorking`, `Next2ScheduledDispatchedWorkingToday`, `NextScheduledDispatchedWorking`, `NextScheduledDispatchedWorkingToday`, `NextScheduledDispatchedWorkingTodayTomorrow`. |
| `jobHistoryDateFilter` | list<string> | no | Appointment history visibility setting. One of: `AllJobs`, `LastMonth`, `LastSevenDays`, `LastThreeDays`. |
| `home` | object | no | Home address object. When supplied, street and city are required. |
| `customFields[]` | array<object> | no | Technician custom-field entries, each with required typeId and optional value. |
| `accountLocked` | boolean | no | Whether the technician account is locked. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | ServiceTitan technician ID updated by the action. |

## Native endpoint

Through the native ServiceTitan API, this operation is `PATCH settings/v2/tenant/{{credentials.tenant}}/technicians/:id` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-technician.md) for the provider-specific parameters and requirements.

