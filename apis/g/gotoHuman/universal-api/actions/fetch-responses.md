# gotoHuman: Fetch Responses

Retrieves past review responses from gotoHuman.

```
GET https://connect.mindcloud.co/v1/universal/gotoHuman/latest/actions/fetch-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a gotoHuman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gotoHuman/latest/actions/fetch-responses?connectionId=$CONNECTION_ID&formId=string&fieldIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "fieldIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gotoHuman/latest/actions/fetch-responses?${params}`, {
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
| `formId` | string | yes | The ID of the review template / form. |
| `fieldIds` | string | yes | Comma-separated field IDs to fetch. |
| `filterResponse` | string | no | Filter by review status: approved or rejected. |
| `groupByField` | boolean | no | Whether to group the responses by field. |
| `approvedValuesOnly` | boolean | no | Return only approved values. |
| `rejectedValuesOnly` | boolean | no | Return only rejected values. |
| `limit` | number | no | Maximum number of responses to return. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filterResponseValues` | string | no | URL-encoded JSON string array used to filter response values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fields": {},
      "respondedAt": "2026-05-07T12:00:00.000Z",
      "response": "string",
      "reviewId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the review request was created. |
| `fields` | object | Field values for the reviewed content, including suggested and approved/rejected values. |
| `respondedAt` | date | When the review was answered. |
| `response` | string | The final human response such as approved or rejected. |
| `reviewId` | string | The review ID. |

## Native endpoint

Through the native gotoHuman API, this operation is `GET /fetchResponses` (base URL `https://api.gotohuman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-responses.md) for the provider-specific parameters and requirements.

