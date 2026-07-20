# Clappia: Get Submission

Retrieves a submission record from Clappia.

```
GET https://connect.mindcloud.co/v1/universal/clappia/latest/actions/get-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clappia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clappia/latest/actions/get-submission?connectionId=$CONNECTION_ID&appId=string&submissionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string",
  "submissionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clappia/latest/actions/get-submission?${params}`, {
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
| `submissionId` | string | yes | Clappia submission ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "createdBy": {},
      "lastModifiedAt": 1,
      "lastModifiedBy": {},
      "owners": [
        {}
      ],
      "status": "string",
      "submissionFieldValues": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `createdBy` | object |  |
| `lastModifiedAt` | number |  |
| `lastModifiedBy` | object |  |
| `owners` | array<object> |  |
| `status` | string |  |
| `submissionFieldValues` | object |  |

## Native endpoint

Through the native Clappia API, this operation is `GET /submissions/getSubmission` (base URL `https://api-public-v4.clappia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-submission.md) for the provider-specific parameters and requirements.

