# Moaform: List Form Responses

Retrieves responses for a form in Moaform.

```
GET https://connect.mindcloud.co/v1/universal/moaform/latest/actions/list-form-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moaform `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moaform/latest/actions/list-form-responses?connectionId=$CONNECTION_ID&limit=25&offset=0&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moaform/latest/actions/list-form-responses?${params}`, {
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
| `formId` | string | yes | Unique ID of the form. |
| `since` | string | no | Only return responses submitted after this timestamp. |
| `until` | string | no | Only return responses submitted before this timestamp. |
| `after` | string | no | Only return responses submitted after this response ID. |
| `before` | string | no | Only return responses submitted before this response ID. |
| `includedResponseIds` | string | no | Comma-separated response IDs to include. |
| `excludedResponseIds` | string | no | Comma-separated response IDs to exclude. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "answers": [
            {
              "block": {
                "id": "string",
                "type": "string"
              },
              "type": "string"
            }
          ],
          "metadata": {
            "browser": "string",
            "device": "string",
            "operatingSystem": "string",
            "userAgent": "string"
          },
          "responseCode": "string",
          "responseId": "string",
          "startedAt": "2026-05-07T12:00:00.000Z",
          "submittedAt": "2026-05-07T12:00:00.000Z",
          "thankyou": {
            "id": "string",
            "url": "https://example.com"
          }
        }
      ],
      "pageCount": 1,
      "totalItems": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `items[].answers` | array<object> |  |
| `items[].answers[].block` | object |  |
| `items[].answers[].block.id` | string |  |
| `items[].answers[].block.type` | string |  |
| `items[].answers[].type` | string |  |
| `items[].metadata` | object |  |
| `items[].metadata.browser` | string |  |
| `items[].metadata.device` | string |  |
| `items[].metadata.operatingSystem` | string |  |
| `items[].metadata.userAgent` | string |  |
| `items[].responseCode` | string |  |
| `items[].responseId` | string |  |
| `items[].startedAt` | date |  |
| `items[].submittedAt` | date |  |
| `items[].thankyou` | object |  |
| `items[].thankyou.id` | string |  |
| `items[].thankyou.url` | string |  |
| `pageCount` | number |  |
| `totalItems` | number |  |

## Native endpoint

Through the native Moaform API, this operation is `GET /forms/:formId/responses` (base URL `https://api.moaform.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-form-responses.md) for the provider-specific parameters and requirements.

