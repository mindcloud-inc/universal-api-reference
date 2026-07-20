# Clappia: Search Submissions

Finds submissions in Clappia by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/clappia/latest/actions/search-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clappia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clappia/latest/actions/search-submissions?connectionId=$CONNECTION_ID&appId=string&requestingUserEmailAddress=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string",
  "requestingUserEmailAddress": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clappia/latest/actions/search-submissions?${params}`, {
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
| `appId` | string | yes | Clappia app ID. |
| `requestingUserEmailAddress` | string | yes | Email address of the Clappia user on whose behalf submissions should be listed. |
| `pageSize` | number | no | Maximum number of submissions to return. Default: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filters` | object | no | Optional Clappia filters object for narrowing returned submissions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lastSubmissionId": "string",
      "metadata": {},
      "submissions": [
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
| `lastSubmissionId` | string |  |
| `metadata` | object |  |
| `submissions` | array<object> |  |

## Native endpoint

Through the native Clappia API, this operation is `POST /submissions/getSubmissions` (base URL `https://api-public-v4.clappia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-submissions.md) for the provider-specific parameters and requirements.

