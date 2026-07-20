# Yousign: List Signature Requests

Retrieves signature requests from Yousign.

```
GET https://connect.mindcloud.co/v1/universal/yousign/latest/actions/list-signature-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yousign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yousign/latest/actions/list-signature-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yousign/latest/actions/list-signature-requests?${params}`, {
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
| `after` | string | no | Pagination cursor. |
| `limit` | number | no | Maximum signature requests to return. |
| `q` | string | no | Search on signature request name. |
| `statusEq` | string | no | Return only signature requests with this exact status. |
| `createdAtAfter` | string | no | Return only signature requests created after this date (yyyy-mm-dd). |
| `createdAtBefore` | string | no | Return only signature requests created before this date (yyyy-mm-dd). |
| `workspaceIdEq` | string | no | Return only signature requests in this workspace. |
| `externalIdEq` | string | no | Return only signature requests with this external ID. |
| `sourceEq` | string | no | Return only signature requests created from this source. |
| `labelNameEq` | string | no | Return only signature requests with a label that exactly matches this name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        [
          {}
        ]
      ],
      "meta": {
        "nextCursor": {}
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | array<object> |  |
| `data[].approvers[]` | array<string> |  |
| `data[].auditTrailLocale` | string |  |
| `data[].brandingId` | object |  |
| `data[].bulkSendBatchId` | object |  |
| `data[].createdAt` | string |  |
| `data[].customExperienceId` | object |  |
| `data[].customProperties[]` | array<string> |  |
| `data[].customRecipientOrder` | boolean |  |
| `data[].deliveryMode` | string |  |
| `data[].documents[]` | array<object> |  |
| `data[].documents[].id` | string |  |
| `data[].documents[].nature` | string |  |
| `data[].emailCustomNote` | object |  |
| `data[].emailNotification` | object |  |
| `data[].emailNotification.customNote` | object |  |
| `data[].emailNotification.customText` | object |  |
| `data[].emailNotification.customText.reminderBody` | object |  |
| `data[].emailNotification.customText.reminderSubject` | object |  |
| `data[].emailNotification.customText.requestBody` | object |  |
| `data[].emailNotification.customText.requestSubject` | object |  |
| `data[].emailNotification.sender` | object |  |
| `data[].emailNotification.sender.customName` | object |  |
| `data[].emailNotification.sender.type` | string |  |
| `data[].expirationDate` | string |  |
| `data[].externalId` | object |  |
| `data[].id` | string |  |
| `data[].labels[]` | array<string> |  |
| `data[].name` | string |  |
| `data[].orderedApprovers` | boolean |  |
| `data[].orderedSigners` | boolean |  |
| `data[].previousAttemptId` | object |  |
| `data[].reminderSettings` | object |  |
| `data[].sender` | object |  |
| `data[].signers[]` | array<object> |  |
| `data[].signers[].customText` | object |  |
| `data[].signers[].customText.reminderBody` | object |  |
| `data[].signers[].customText.reminderSubject` | object |  |
| `data[].signers[].customText.requestBody` | object |  |
| `data[].signers[].customText.requestSubject` | object |  |
| `data[].signers[].deliveryMode` | string |  |
| `data[].signers[].id` | string |  |
| `data[].signers[].status` | string |  |
| `data[].signersAllowedToDecline` | boolean |  |
| `data[].source` | string |  |
| `data[].status` | string |  |
| `data[].timezone` | string |  |
| `data[].workflowSessionId` | object |  |
| `data[].workspaceId` | string |  |
| `meta` | object |  |
| `meta.nextCursor` | object |  |

## Native endpoint

Through the native Yousign API, this operation is `GET /signature_requests` (base URL `https://api-sandbox.yousign.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-signature-requests.md) for the provider-specific parameters and requirements.

