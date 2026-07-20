# Formbricks: Get Responses

Retrieves responses from Formbricks.

```
GET https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/get-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formbricks `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/get-responses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/get-responses?${params}`, {
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
| `limit` | number | no |  |
| `skip` | number | no |  |
| `sortBy` | string | no |  |
| `order` | string | no |  |
| `startDate` | date | no |  |
| `endDate` | date | no |  |
| `filterDateField` | string | no |  |
| `surveyId` | string | no |  |
| `contactId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "contactAttributes": {},
          "contactId": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "data": {},
          "displayId": "string",
          "endingId": "string",
          "finished": true,
          "id": "string",
          "language": "string",
          "meta": {},
          "singleUseId": "string",
          "surveyId": "string",
          "ttc": {},
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "variables": {}
        }
      ],
      "meta": {
        "limit": 1,
        "offset": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Responses returned by the management API. |
| `data[].contactAttributes` | object | Snapshot of contact attributes on the response. |
| `data[].contactId` | string | Contact ID associated with the response. |
| `data[].createdAt` | date | Creation timestamp. |
| `data[].data` | object | Submitted response payload. |
| `data[].displayId` | string | Display ID associated with the response. |
| `data[].endingId` | string | Ending ID associated with the response. |
| `data[].finished` | boolean | Whether the response is finished. |
| `data[].id` | string | Response ID. |
| `data[].language` | string | Language used for the response. |
| `data[].meta` | object | Response metadata such as source and user agent. |
| `data[].singleUseId` | string | Single-use link identifier when present. |
| `data[].surveyId` | string | Survey ID associated with the response. |
| `data[].ttc` | object | Time-to-complete metrics by question. |
| `data[].updatedAt` | date | Last update timestamp. |
| `data[].variables` | object | Captured survey variables. |
| `meta` | object | Pagination metadata. |
| `meta.limit` | number | Applied page size. |
| `meta.offset` | number | Applied offset. |
| `meta.total` | number | Total number of matching responses. |

## Native endpoint

Through the native Formbricks API, this operation is `GET /management/responses` (base URL `https://app.formbricks.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-responses.md) for the provider-specific parameters and requirements.

