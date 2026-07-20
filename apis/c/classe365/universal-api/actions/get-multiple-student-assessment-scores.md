# Classe365: Get Multiple Student Assessment Scores

Retrieves assessment scores for multiple students from Classe365.

```
GET https://connect.mindcloud.co/v1/universal/classe365/latest/actions/get-multiple-student-assessment-scores
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Classe365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/get-multiple-student-assessment-scores?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/classe365/latest/actions/get-multiple-student-assessment-scores?${params}`, {
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
      "assessmentId": 1,
      "score": "string",
      "studentId": 1,
      "subjectId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assessmentId` | number |  |
| `score` | string |  |
| `studentId` | number |  |
| `subjectId` | number |  |

## Native endpoint

Through the native Classe365 API, this operation is `GET /rest/studentsScore` (base URL `https://{{credentials.username}}.classe365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-multiple-student-assessment-scores.md) for the provider-specific parameters and requirements.

