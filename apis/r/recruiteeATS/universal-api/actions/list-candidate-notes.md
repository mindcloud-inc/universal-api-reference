# Recruitee ATS: List Candidate Notes



```
GET https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/list-candidate-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recruitee ATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/list-candidate-notes?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/list-candidate-notes?${params}`, {
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
| `id` | number | yes | Candidate ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminId": 1,
      "body": "string",
      "bodyHtml": "string",
      "bodyJson": {
        "doc": {
          "content": [
            {
              "content": [
                {
                  "text": "string",
                  "type": "string"
                }
              ],
              "type": "string"
            }
          ],
          "type": "string"
        }
      },
      "candidateId": 1,
      "createdAt": "string",
      "guestId": {},
      "id": 1,
      "offerId": {},
      "pinnedAt": {},
      "replyToId": {},
      "requisitionId": {},
      "talentPoolId": {},
      "text": "string",
      "triggered": true,
      "updatedAt": "string",
      "visibility": {
        "level": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminId` | number |  |
| `body` | string |  |
| `bodyHtml` | string |  |
| `bodyJson.doc.content[].content[].text` | string |  |
| `bodyJson.doc.content[].content[].type` | string |  |
| `bodyJson.doc.content[].type` | string |  |
| `bodyJson.doc.type` | string |  |
| `candidateId` | number |  |
| `createdAt` | string |  |
| `guestId` | object |  |
| `id` | number |  |
| `offerId` | object |  |
| `pinnedAt` | object |  |
| `replyToId` | object |  |
| `requisitionId` | object |  |
| `talentPoolId` | object |  |
| `text` | string |  |
| `triggered` | boolean |  |
| `updatedAt` | string |  |
| `visibility.level` | string |  |

## Native endpoint

Through the native Recruitee ATS API, this operation is `GET /c/:company_id/candidates/:id/notes` (base URL `https://api.recruitee.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-candidate-notes.md) for the provider-specific parameters and requirements.

