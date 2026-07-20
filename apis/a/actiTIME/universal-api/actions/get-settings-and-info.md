# actiTIME: Get Settings and Info

Retrieves workspace settings and info from actiTIME.

```
GET https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-settings-and-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a actiTIME `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-settings-and-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-settings-and-info?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {
        "logoUri": "string",
        "name": "Ava Chen"
      },
      "customNames": {
        "department": {
          "plural": "Ava Chen",
          "singular": "Ava Chen"
        },
        "firstLevel": {
          "plural": "Ava Chen",
          "singular": "Ava Chen"
        },
        "secondLevel": {
          "plural": "Ava Chen",
          "singular": "Ava Chen"
        },
        "thirdLevel": {
          "plural": "Ava Chen",
          "singular": "Ava Chen"
        }
      },
      "features": {
        "departments": true,
        "leavetimeRegistration": true,
        "overtimeRegistration": true,
        "taskEstimates": true,
        "taskWorkflow": true,
        "timeZoneGroups": true,
        "typesOfWork": true,
        "workAssignments": true
      },
      "format": {
        "clockFormat": "string",
        "currency": "string",
        "dayOfWeekStart": 1,
        "decimalSeparator": "string",
        "timeFormat": "string"
      },
      "limits": {
        "maxBatchSize": 1,
        "maxQueryLimit": 1
      },
      "serverUUID": "string",
      "urls": {
        "actiPlans": "https://example.com",
        "actiTime": "https://example.com",
        "api": "https://example.com",
        "apiDocumentation": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company.logoUri` | string | Company logo URL. |
| `company.name` | string | Company name. |
| `customNames.department.plural` | string | Plural department label. |
| `customNames.department.singular` | string | Singular department label. |
| `customNames.firstLevel.plural` | string | Plural label for the first hierarchy level. |
| `customNames.firstLevel.singular` | string | Singular label for the first hierarchy level. |
| `customNames.secondLevel.plural` | string | Plural label for the second hierarchy level. |
| `customNames.secondLevel.singular` | string | Singular label for the second hierarchy level. |
| `customNames.thirdLevel.plural` | string | Plural label for the third hierarchy level. |
| `customNames.thirdLevel.singular` | string | Singular label for the third hierarchy level. |
| `features.departments` | boolean | Whether departments are enabled. |
| `features.leavetimeRegistration` | boolean | Whether leave-time registration is enabled. |
| `features.overtimeRegistration` | boolean | Whether overtime registration is enabled. |
| `features.taskEstimates` | boolean | Whether task estimates are enabled. |
| `features.taskWorkflow` | boolean | Whether task workflow is enabled. |
| `features.timeZoneGroups` | boolean | Whether time zone groups are enabled. |
| `features.typesOfWork` | boolean | Whether types of work are enabled. |
| `features.workAssignments` | boolean | Whether work assignments are enabled. |
| `format.clockFormat` | string | Preferred clock format. |
| `format.currency` | string | Workspace currency symbol. |
| `format.dayOfWeekStart` | number | Day index used as the start of the week. |
| `format.decimalSeparator` | string | Decimal separator. |
| `format.timeFormat` | string | Preferred time format. |
| `limits.maxBatchSize` | number | Maximum batch size. |
| `limits.maxQueryLimit` | number | Maximum query limit. |
| `serverUUID` | string | Server instance identifier. |
| `urls.actiPlans` | string | actiPLANS application URL. |
| `urls.actiTime` | string | actiTIME application URL. |
| `urls.api` | string | API base URL. |
| `urls.apiDocumentation` | string | API documentation URL. |

## Native endpoint

Through the native actiTIME API, this operation is `GET /info` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-settings-and-info.md) for the provider-specific parameters and requirements.

