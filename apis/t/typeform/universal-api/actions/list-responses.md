# Typeform: List Responses



```
GET https://connect.mindcloud.co/v1/universal/typeform/latest/actions/list-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeform/latest/actions/list-responses?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typeform/latest/actions/list-responses?${params}`, {
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
| `excludedResponseIds` | string | no |  |
| `formId` | list | yes | Typeform form ID. |
| `responseType` | string | no |  |
| `sort` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `since` | date | no | Return responses submitted after this date/time. |
| `until` | date | no | Return responses submitted before this date/time. |
| `after` | string | no | Cursor token for next page of responses. |
| `before` | string | no | Cursor token for previous page of responses. |
| `completed` | boolean | no | Filter by completion status. |
| `query` | string | no | Search responses by text. |
| `fields` | string | no | Filter on specific field IDs. Accepts multiple values in one string, delimited by `,`. |
| `answeredFields` | string | no | Filter by answered field IDs. Accepts multiple values in one string, delimited by `,`. |
| `includedResponseIds` | string | no | Only include specific response IDs. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answers": [
        {
          "boolean": true,
          "choice": {
            "label": "string"
          },
          "choices": {
            "labels": [
              "string"
            ]
          },
          "date": "2026-05-07T12:00:00.000Z",
          "email": "ava@example.com",
          "field": {
            "id": "string",
            "ref": "string",
            "type": "string"
          },
          "fileUrl": "https://example.com",
          "number": 1,
          "text": "string",
          "type": "string",
          "url": "https://example.com"
        }
      ],
      "calculated": {
        "score": 1
      },
      "definition": {
        "fields": [
          {
            "id": "string",
            "ref": "string",
            "title": "string",
            "type": "string"
          }
        ],
        "id": "string",
        "title": "string"
      },
      "ending": {
        "id": "string",
        "ref": "string"
      },
      "hidden": {
        "value": "string"
      },
      "landedAt": "2026-05-07T12:00:00.000Z",
      "landingId": "string",
      "metadata": {
        "browser": "string",
        "networkId": "string",
        "platform": "string",
        "referer": "string",
        "userAgent": "string"
      },
      "responseId": "string",
      "submittedAt": "2026-05-07T12:00:00.000Z",
      "token": "string",
      "variables": [
        {
          "boolean": true,
          "id": "string",
          "key": "string",
          "number": 1,
          "text": "string",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answers` | array<object> | Response answers. |
| `answers[].boolean` | boolean | Boolean answer value. |
| `answers[].choice` | object | Single-choice answer payload. |
| `answers[].choice.label` | string | Single-choice label. |
| `answers[].choices` | object | Multiple-choice answer payload. |
| `answers[].choices.labels` | array<string> | Multiple-choice selected labels. |
| `answers[].date` | date | Date answer value. |
| `answers[].email` | string | Email answer value. |
| `answers[].field` | object | Field metadata for this answer. |
| `answers[].field.id` | string | Field ID. |
| `answers[].field.ref` | string | Field reference. |
| `answers[].field.type` | string | Field type. |
| `answers[].fileUrl` | string | Uploaded file URL. |
| `answers[].number` | number | Numeric answer value. |
| `answers[].text` | string | Text answer value. |
| `answers[].type` | string | Answer type. |
| `answers[].url` | string | URL answer value. |
| `calculated` | object | Calculated values. |
| `calculated.score` | number | Calculated score. |
| `definition` | object | Form definition snapshot. |
| `definition.fields` | array<object> | Form fields at response time. |
| `definition.fields[].id` | string | Field ID. |
| `definition.fields[].ref` | string | Field reference. |
| `definition.fields[].title` | string | Field title. |
| `definition.fields[].type` | string | Field type. |
| `definition.id` | string | Form definition ID. |
| `definition.title` | string | Form title at response time. |
| `ending` | object | Ending details. |
| `ending.id` | string | Ending ID. |
| `ending.ref` | string | Ending reference. |
| `hidden` | object | Hidden field values keyed by hidden variable name. |
| `hidden.value` | string | One hidden field value. |
| `landedAt` | date | Landing timestamp. |
| `landingId` | string | Landing ID. |
| `metadata` | object | Response metadata. |
| `metadata.browser` | string | Browser name. |
| `metadata.networkId` | string | Network identifier. |
| `metadata.platform` | string | Submitting platform. |
| `metadata.referer` | string | Referrer URL. |
| `metadata.userAgent` | string | User agent string. |
| `responseId` | string | Response ID. |
| `submittedAt` | date | Submission timestamp. |
| `token` | string | Response token. |
| `variables` | array<object> | Variable values. |
| `variables[].boolean` | boolean | Variable boolean value. |
| `variables[].id` | string | Variable ID. |
| `variables[].key` | string | Variable key. |
| `variables[].number` | number | Variable numeric value. |
| `variables[].text` | string | Variable text value. |
| `variables[].type` | string | Variable type. |

## Native endpoint

Through the native Typeform API, this operation is `GET /forms/:formId/responses` (base URL `https://api.typeform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-responses.md) for the provider-specific parameters and requirements.

