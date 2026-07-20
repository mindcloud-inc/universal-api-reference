# Productive.io: Get Booking

Retrieves a booking from your Productive.io account.

```
GET https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/get-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productive.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/get-booking?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/get-booking?${params}`, {
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
| `id` | string | yes | The Productive resource ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "approved": true,
        "approvedAt": "string",
        "autotracking": true,
        "bookingMethodId": 1,
        "canceled": true,
        "canceledAt": "string",
        "createdAt": "string",
        "customFields": "string",
        "draft": true,
        "endedOn": "string",
        "externalId": "string",
        "hours": 1,
        "lastActivityAt": "string",
        "note": "string",
        "peopleCustomFields": "string",
        "percentage": 1,
        "rejected": true,
        "rejectedAt": "string",
        "rejectedReason": "string",
        "stageType": 1,
        "startedOn": "string",
        "time": 1,
        "totalTime": 1,
        "totalWorkingDays": 1,
        "updatedAt": "string"
      },
      "id": "string",
      "relationships": {
        "approvalStatuses": {
          "meta": {
            "included": true
          }
        },
        "approver": {
          "meta": {
            "included": true
          }
        },
        "attachments": {
          "meta": {
            "included": true
          }
        },
        "canceler": {
          "meta": {
            "included": true
          }
        },
        "creator": {
          "meta": {
            "included": true
          }
        },
        "customFieldAttachments": {
          "meta": {
            "included": true
          }
        },
        "customFieldPeople": {
          "meta": {
            "included": true
          }
        },
        "event": {
          "meta": {
            "included": true
          }
        },
        "organization": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "origin": {
          "meta": {
            "included": true
          }
        },
        "person": {
          "meta": {
            "included": true
          }
        },
        "rejecter": {
          "meta": {
            "included": true
          }
        },
        "service": {
          "meta": {
            "included": true
          }
        },
        "updater": {
          "meta": {
            "included": true
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.approved` | boolean |  |
| `attributes.approvedAt` | string |  |
| `attributes.autotracking` | boolean |  |
| `attributes.bookingMethodId` | number |  |
| `attributes.canceled` | boolean |  |
| `attributes.canceledAt` | string |  |
| `attributes.createdAt` | string |  |
| `attributes.customFields` | string |  |
| `attributes.draft` | boolean |  |
| `attributes.endedOn` | string |  |
| `attributes.externalId` | string |  |
| `attributes.hours` | number |  |
| `attributes.lastActivityAt` | string |  |
| `attributes.note` | string |  |
| `attributes.peopleCustomFields` | string |  |
| `attributes.percentage` | number |  |
| `attributes.rejected` | boolean |  |
| `attributes.rejectedAt` | string |  |
| `attributes.rejectedReason` | string |  |
| `attributes.stageType` | number |  |
| `attributes.startedOn` | string |  |
| `attributes.time` | number |  |
| `attributes.totalTime` | number |  |
| `attributes.totalWorkingDays` | number |  |
| `attributes.updatedAt` | string |  |
| `id` | string |  |
| `relationships.approvalStatuses.meta.included` | boolean |  |
| `relationships.approver.meta.included` | boolean |  |
| `relationships.attachments.meta.included` | boolean |  |
| `relationships.canceler.meta.included` | boolean |  |
| `relationships.creator.meta.included` | boolean |  |
| `relationships.customFieldAttachments.meta.included` | boolean |  |
| `relationships.customFieldPeople.meta.included` | boolean |  |
| `relationships.event.meta.included` | boolean |  |
| `relationships.organization.data.id` | string |  |
| `relationships.organization.data.type` | string |  |
| `relationships.origin.meta.included` | boolean |  |
| `relationships.person.meta.included` | boolean |  |
| `relationships.rejecter.meta.included` | boolean |  |
| `relationships.service.meta.included` | boolean |  |
| `relationships.updater.meta.included` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Productive.io API, this operation is `GET /bookings/{{id}}` (base URL `https://api.productive.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-booking.md) for the provider-specific parameters and requirements.

