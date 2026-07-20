# Mona AI: Parse Applicant CV

Parses an applicant CV in Mona AI.

```
GET https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/parse-applicant-cv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mona AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/parse-applicant-cv?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/parse-applicant-cv?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mona AI API returns.

## Native endpoint

Through the native Mona AI API, this operation is `POST /parsing/parseApplicantCV` (base URL `https://api.mona-ai.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-applicant-cv.md) for the provider-specific parameters and requirements.

