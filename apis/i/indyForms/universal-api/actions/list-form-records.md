# IndyForms: List Form Records



```
GET https://connect.mindcloud.co/v1/universal/indyForms/latest/actions/list-form-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IndyForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/indyForms/latest/actions/list-form-records?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/indyForms/latest/actions/list-form-records?${params}`, {
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
| `formId` | string | yes |  |
| `submitted` | boolean | no |  |
| `createdAt.from` | date | no |  |
| `createdAt.to` | date | no |  |
| `submittedAt.from` | date | no |  |
| `submittedAt.to` | date | no |  |
| `keywords` | string | no |  |
| `rangeStart` | number | no |  |
| `rangeEnd` | number | no |  |
| `includeResponseData` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contributors": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "data": {},
      "dueAt": "2026-05-07T12:00:00.000Z",
      "form": {},
      "id": "string",
      "lastEditedAt": "2026-05-07T12:00:00.000Z",
      "submittedAt": "2026-05-07T12:00:00.000Z",
      "submittedBy": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contributors` | array<object> |  |
| `createdAt` | date |  |
| `createdBy` | object |  |
| `data` | object |  |
| `dueAt` | date |  |
| `form` | object |  |
| `id` | string |  |
| `lastEditedAt` | date |  |
| `submittedAt` | date |  |
| `submittedBy` | object |  |

## Native endpoint

Through the native IndyForms API, this operation is `GET /api/public/v2/forms/:formId/records` (base URL `https://api.indyforms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-records.md) for the provider-specific parameters and requirements.

