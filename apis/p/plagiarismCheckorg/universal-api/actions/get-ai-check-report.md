# PlagiarismCheck.org: Get AI Check Report



```
GET https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/get-ai-check-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlagiarismCheck.org `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/get-ai-check-report?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/get-ai-check-report?${params}`, {
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
| `id` | number | yes | AI check identifier returned by Submit AI Check From Text or Submit AI Check From File. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "comment": {},
        "commentAuthor": {},
        "conclusion": "string",
        "conclusionType": 1,
        "createdAt": 1,
        "creator": {
          "aiChecksEnabled": true,
          "allowedLanguages": [
            "string"
          ],
          "avatar": "string",
          "balance": {
            "aiBalance": 1,
            "balance": 1,
            "bonus": 1,
            "hold": 1,
            "holdBonus": 1
          },
          "balanceType": 1,
          "createdAt": "string",
          "email": "ava@example.com",
          "id": 1,
          "isBlocked": true,
          "isChangePasswordNeeded": true,
          "isEmailVerificationNeeded": true,
          "isGuest": true,
          "lastAiOrderPaidDaysAgo": {},
          "name": "Ava Chen",
          "notAiOrders": 1,
          "orders": 1,
          "saleRole": {},
          "updatedAt": "string"
        },
        "enabled": true,
        "groupId": {},
        "hasOwnContent": true,
        "id": 1,
        "likelyPercent": {},
        "mark": {},
        "pages": {},
        "percent": {},
        "processedPercent": "string",
        "status": 1,
        "strongPercent": {},
        "type": 1,
        "words": {}
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.comment` | object |  |
| `data.commentAuthor` | object |  |
| `data.conclusion` | string |  |
| `data.conclusionType` | number |  |
| `data.createdAt` | number |  |
| `data.creator.aiChecksEnabled` | boolean |  |
| `data.creator.allowedLanguages[]` | string |  |
| `data.creator.avatar` | string |  |
| `data.creator.balance.aiBalance` | number |  |
| `data.creator.balance.balance` | number |  |
| `data.creator.balance.bonus` | number |  |
| `data.creator.balance.hold` | number |  |
| `data.creator.balance.holdBonus` | number |  |
| `data.creator.balanceType` | number |  |
| `data.creator.createdAt` | string |  |
| `data.creator.email` | string |  |
| `data.creator.id` | number |  |
| `data.creator.isBlocked` | boolean |  |
| `data.creator.isChangePasswordNeeded` | boolean |  |
| `data.creator.isEmailVerificationNeeded` | boolean |  |
| `data.creator.isGuest` | boolean |  |
| `data.creator.lastAiOrderPaidDaysAgo` | object |  |
| `data.creator.name` | string |  |
| `data.creator.notAiOrders` | number |  |
| `data.creator.orders` | number |  |
| `data.creator.saleRole` | object |  |
| `data.creator.updatedAt` | string |  |
| `data.enabled` | boolean |  |
| `data.groupId` | object |  |
| `data.hasOwnContent` | boolean |  |
| `data.id` | number |  |
| `data.likelyPercent` | object |  |
| `data.mark` | object |  |
| `data.pages` | object |  |
| `data.percent` | object |  |
| `data.processedPercent` | string |  |
| `data.status` | number |  |
| `data.strongPercent` | object |  |
| `data.type` | number |  |
| `data.words` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native PlagiarismCheck.org API, this operation is `GET /api/v1/chat-gpt/:id` (base URL `https://plagiarismcheck.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ai-check-report.md) for the provider-specific parameters and requirements.

