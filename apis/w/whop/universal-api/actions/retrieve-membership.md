# Whop: Retrieve Membership

Retrieves membership details from the Whop platform.

```
GET https://connect.mindcloud.co/v1/universal/whop/latest/actions/retrieve-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whop/latest/actions/retrieve-membership?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whop/latest/actions/retrieve-membership?${params}`, {
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
| `id` | string | yes | The unique identifier of the membership. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancelAtPeriodEnd": true,
      "canceledAt": "2026-05-07T12:00:00.000Z",
      "cancellationReason": "string",
      "cancelOption": "string",
      "company": {
        "id": "string",
        "title": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "customFieldResponses": [
        {
          "answer": "string",
          "id": "string",
          "question": "string"
        }
      ],
      "id": "string",
      "joinedAt": "2026-05-07T12:00:00.000Z",
      "licenseKey": "string",
      "manageUrl": "https://example.com",
      "member": {
        "id": "string"
      },
      "paymentCollectionPaused": true,
      "plan": {
        "id": "string"
      },
      "product": {
        "id": "string",
        "title": "string"
      },
      "promoCode": {
        "id": "string"
      },
      "renewalPeriodEnd": "2026-05-07T12:00:00.000Z",
      "renewalPeriodStart": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen",
        "username": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancelAtPeriodEnd` | boolean |  |
| `canceledAt` | date |  |
| `cancellationReason` | string |  |
| `cancelOption` | string |  |
| `company` | object |  |
| `company.id` | string |  |
| `company.title` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `customFieldResponses` | array<object> |  |
| `customFieldResponses[].answer` | string |  |
| `customFieldResponses[].id` | string |  |
| `customFieldResponses[].question` | string |  |
| `id` | string |  |
| `joinedAt` | date |  |
| `licenseKey` | string |  |
| `manageUrl` | string |  |
| `member` | object |  |
| `member.id` | string |  |
| `paymentCollectionPaused` | boolean |  |
| `plan` | object |  |
| `plan.id` | string |  |
| `product` | object |  |
| `product.id` | string |  |
| `product.title` | string |  |
| `promoCode` | object |  |
| `promoCode.id` | string |  |
| `renewalPeriodEnd` | date |  |
| `renewalPeriodStart` | date |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `user` | object |  |
| `user.email` | string |  |
| `user.id` | string |  |
| `user.name` | string |  |
| `user.username` | string |  |

## Native endpoint

Through the native Whop API, this operation is `GET /api/v1/memberships/:id` (base URL `https://api.whop.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-membership.md) for the provider-specific parameters and requirements.

