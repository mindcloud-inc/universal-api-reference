# TalentHR: Get Benefit Filters

Retrieves benefit filters from TalentHR.

```
GET https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-benefit-filters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-benefit-filters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-benefit-filters?${params}`, {
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
      "departments": [
        {}
      ],
      "divisions": [
        {}
      ],
      "employees": [
        {}
      ],
      "empState": [
        {}
      ],
      "jobTitles": [
        {}
      ],
      "locations": [
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
| `departments` | array<object> |  |
| `divisions` | array<object> |  |
| `employees` | array<object> |  |
| `empState` | array<object> |  |
| `jobTitles` | array<object> |  |
| `locations` | array<object> |  |

## Native endpoint

Through the native TalentHR API, this operation is `GET /benefits/filters` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-benefit-filters.md) for the provider-specific parameters and requirements.

