# PlagiarismCheck.org: Get Plagiarism Check Status



```
GET https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/get-plagiarism-check-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlagiarismCheck.org `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/get-plagiarism-check-status?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/get-plagiarism-check-status?${params}`, {
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
| `id` | number | yes | Plagiarism check identifier returned by Submit Plagiarism Check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "aiReport": {
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
        "createdAt": "string",
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
        "customAuthor": {},
        "deletedAt": {},
        "filename": "Ava Chen",
        "groupId": {},
        "id": 1,
        "isDeleted": true,
        "language": "string",
        "pages": 1,
        "report": {
          "createdAt": "string",
          "id": 1,
          "percent": "string",
          "sourceCount": 1,
          "version": {}
        },
        "state": 1,
        "submittedAt": "string",
        "updatedAt": "string",
        "version": {},
        "words": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.aiReport.comment` | object |  |
| `data.aiReport.commentAuthor` | object |  |
| `data.aiReport.conclusion` | string |  |
| `data.aiReport.conclusionType` | number |  |
| `data.aiReport.createdAt` | number |  |
| `data.aiReport.creator.aiChecksEnabled` | boolean |  |
| `data.aiReport.creator.allowedLanguages[]` | string |  |
| `data.aiReport.creator.avatar` | string |  |
| `data.aiReport.creator.balance.aiBalance` | number |  |
| `data.aiReport.creator.balance.balance` | number |  |
| `data.aiReport.creator.balance.bonus` | number |  |
| `data.aiReport.creator.balance.hold` | number |  |
| `data.aiReport.creator.balance.holdBonus` | number |  |
| `data.aiReport.creator.balanceType` | number |  |
| `data.aiReport.creator.createdAt` | string |  |
| `data.aiReport.creator.email` | string |  |
| `data.aiReport.creator.id` | number |  |
| `data.aiReport.creator.isBlocked` | boolean |  |
| `data.aiReport.creator.isChangePasswordNeeded` | boolean |  |
| `data.aiReport.creator.isEmailVerificationNeeded` | boolean |  |
| `data.aiReport.creator.isGuest` | boolean |  |
| `data.aiReport.creator.lastAiOrderPaidDaysAgo` | object |  |
| `data.aiReport.creator.name` | string |  |
| `data.aiReport.creator.notAiOrders` | number |  |
| `data.aiReport.creator.orders` | number |  |
| `data.aiReport.creator.saleRole` | object |  |
| `data.aiReport.creator.updatedAt` | string |  |
| `data.aiReport.enabled` | boolean |  |
| `data.aiReport.groupId` | object |  |
| `data.aiReport.hasOwnContent` | boolean |  |
| `data.aiReport.id` | number |  |
| `data.aiReport.likelyPercent` | object |  |
| `data.aiReport.mark` | object |  |
| `data.aiReport.pages` | object |  |
| `data.aiReport.percent` | object |  |
| `data.aiReport.processedPercent` | string |  |
| `data.aiReport.status` | number |  |
| `data.aiReport.strongPercent` | object |  |
| `data.aiReport.type` | number |  |
| `data.aiReport.words` | object |  |
| `data.createdAt` | string |  |
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
| `data.customAuthor` | object |  |
| `data.deletedAt` | object |  |
| `data.filename` | string |  |
| `data.groupId` | object |  |
| `data.id` | number |  |
| `data.isDeleted` | boolean |  |
| `data.language` | string |  |
| `data.pages` | number |  |
| `data.report.createdAt` | string |  |
| `data.report.id` | number |  |
| `data.report.percent` | string |  |
| `data.report.sourceCount` | number |  |
| `data.report.version` | object |  |
| `data.state` | number |  |
| `data.submittedAt` | string |  |
| `data.updatedAt` | string |  |
| `data.version` | object |  |
| `data.words` | number |  |

## Native endpoint

Through the native PlagiarismCheck.org API, this operation is `GET /api/v1/text/:id` (base URL `https://plagiarismcheck.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-plagiarism-check-status.md) for the provider-specific parameters and requirements.

