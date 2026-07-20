# Survser: List Surveys



```
GET https://connect.mindcloud.co/v1/universal/survser/latest/actions/list-surveys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Survser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/survser/latest/actions/list-surveys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/survser/latest/actions/list-surveys?${params}`, {
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
      "createdAt": "string",
      "displayCount": 1,
      "id": "string",
      "name": "Ava Chen",
      "questions": [
        {}
      ],
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | When the survey was created. |
| `displayCount` | number | How many times the survey has been displayed. |
| `id` | string | The Survser survey ID. |
| `name` | string | The survey name. |
| `questions` | array<object> | Survey question definitions returned by Survser. |
| `status` | string | The survey status. |
| `updatedAt` | string | When the survey was last updated. |

## Native endpoint

Through the native Survser API, this operation is `GET /survey/list` (base URL `https://survser.com/api/public/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-surveys.md) for the provider-specific parameters and requirements.

