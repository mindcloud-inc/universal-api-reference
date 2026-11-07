# ServiceTitan: Create Technician



```
POST https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-technician
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-technician" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "accountCreationMethod": "AssignLoginAndPassword",
  "roleId": 1,
  "positions[]": [
    "string"
  ],
  "licenseType": "ManagedInstaller"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-technician', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "accountCreationMethod": "AssignLoginAndPassword",
    "roleId": 1,
    "positions[]": ["string"],
    "licenseType": "ManagedInstaller"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customFields[].typeId` | number | no |  |
| `name` | string | yes | Technician name. |
| `customFields[].name` | string | no |  |
| `phoneNumber` | string | no | Technician phone number. |
| `customFields[].value` | string | no |  |
| `email` | string | no | Technician email address. |
| `login` | string | no | Login username. |
| `password` | string | no | Password when Account Creation Method is AssignLoginAndPassword. |
| `accountCreationMethod` | list<string> | yes | How to create the technician account: CreateLater, SendInvite, or AssignLoginAndPassword. One of: `AssignLoginAndPassword`, `CreateLater`, `SendInvite`. |
| `businessUnitId` | number | no | Business unit ID. |
| `roleId` | number | yes | User role ID. |
| `positions[]` | array<string> | yes | Company positions. Allowed values: Installer, Service, Sales, Maintenance, Helper, InstallProductionManager, ServiceManager, SalesManager, PartRunner, DummyTech. |
| `licenseType` | list<string> | yes | Technician license type: NonManagedTech, ManagedTech, or ManagedInstaller. One of: `ManagedInstaller`, `ManagedTech`, `NonManagedTech`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mainZoneId` | number | no | Main technician zone ID. |
| `zoneIds[]` | array<number> | no | All technician zone IDs. Sending this field replaces the existing zone list. |
| `projectLabelIds[]` | array<number> | no | Project label IDs. Requires the Budget vs Actual feature flag. |
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
| `id` | number | ServiceTitan technician ID created by the action. |

## Native endpoint

Through the native ServiceTitan API, this operation is `POST settings/v2/tenant/{{credentials.tenant}}/technicians` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-technician.md) for the provider-specific parameters and requirements.

