# AidaForm: List Responses

Retrieves form responses from AidaForm by form ID.

```
GET https://connect.mindcloud.co/v1/universal/aidaForm/latest/actions/list-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AidaForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aidaForm/latest/actions/list-responses?connectionId=$CONNECTION_ID&formId=61bdb4a6-fb25-4400-952b-a5d74604f90f" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "61bdb4a6-fb25-4400-952b-a5d74604f90f"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aidaForm/latest/actions/list-responses?${params}`, {
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
| `formId` | string | yes | Use the top-level form UUID from List Forms.id. Do not use the short code in data.code. Example: `61bdb4a6-fb25-4400-952b-a5d74604f90f`. |
| `from` | number | no | Only include responses not older than this Unix timestamp. |
| `to` | number | no | Only include responses not newer than this Unix timestamp. |
| `limit` | number | no | Maximum number of responses to return. |
| `marker` | string | no | Pagination marker for the next page of responses. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "items": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "fields": [
            {
              "label": "string",
              "type": "string",
              "values": [
                "string"
              ]
            }
          ],
          "id": "string",
          "reference": "string",
          "referenceStatus": {},
          "unread": {}
        }
      ],
      "marker": {},
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `items[].createdAt` | date |  |
| `items[].fields[].label` | string |  |
| `items[].fields[].type` | string |  |
| `items[].fields[].values[]` | string |  |
| `items[].id` | string |  |
| `items[].reference` | string |  |
| `items[].referenceStatus` | object |  |
| `items[].unread` | object |  |
| `marker` | object |  |
| `total` | number |  |

## Native endpoint

Through the native AidaForm API, this operation is `GET /forms/:formId/responses` (base URL `https://api.aidaform.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-responses.md) for the provider-specific parameters and requirements.

