# TalentHR: Get Directory Filters

Retrieves employee directory filters from TalentHR.

```
GET https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-directory-filters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-directory-filters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-directory-filters?${params}`, {
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
      "empState": [
        {}
      ],
      "locations": [
        {}
      ],
      "timeOffTypes": [
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
| `departments` | array<object> | Department filter options. |
| `divisions` | array<object> | Division filter options. |
| `empState` | array<object> | Employment status filter options. |
| `locations` | array<object> | Location filter options. |
| `timeOffTypes` | array<object> | Time off type filter options. |

## Native endpoint

Through the native TalentHR API, this operation is `GET /directory/filters` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-directory-filters.md) for the provider-specific parameters and requirements.

