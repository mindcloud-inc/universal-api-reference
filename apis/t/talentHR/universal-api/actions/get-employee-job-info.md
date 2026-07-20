# TalentHR: Get Employee Job Info

Retrieves employee job details from TalentHR.

```
GET https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-employee-job-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-employee-job-info?connectionId=$CONNECTION_ID&employee=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employee": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-employee-job-info?${params}`, {
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
| `employee` | number | yes | TalentHR employee ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "benefits": [
        {}
      ],
      "compensationRecords": [
        {}
      ],
      "employmentStatuses": [
        {}
      ],
      "jobRecords": [
        {}
      ],
      "managerRecords": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `benefits` | array<object> |  |
| `compensationRecords` | array<object> |  |
| `employmentStatuses` | array<object> |  |
| `jobRecords` | array<object> |  |
| `managerRecords` | array<object> |  |

## Native endpoint

Through the native TalentHR API, this operation is `GET /employees/:employee/job` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee-job-info.md) for the provider-specific parameters and requirements.

