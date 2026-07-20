# Productive.io: Get Time Entry

Retrieves a time entry from your Productive.io account.

```
GET https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/get-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productive.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/get-time-entry?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/get-time-entry?${params}`, {
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
        "billableTime": 1,
        "calendarEventId": "string",
        "cost": 1,
        "costDefault": 1,
        "costNormalized": 1,
        "createdAt": "string",
        "currency": "string",
        "currencyDefault": "string",
        "currencyNormalized": "string",
        "date": "string",
        "facilityOverheadCost": 1,
        "facilityOverheadCostDefault": 1,
        "facilityOverheadCostNormalized": 1,
        "internalOverheadCost": 1,
        "internalOverheadCostDefault": 1,
        "internalOverheadCostNormalized": 1,
        "invoiceAttributionId": "string",
        "invoiced": true,
        "lastActivityAt": "string",
        "note": "string",
        "overhead": true,
        "overheadCost": 1,
        "overheadCostDefault": 1,
        "overheadCostNormalized": 1,
        "recognizedTime": 1,
        "rejected": true,
        "rejectedAt": "string",
        "rejectedReason": "string",
        "startedAt": "string",
        "submitted": true,
        "time": 1,
        "timerStartedAt": "string",
        "timerStoppedAt": "string",
        "trackMethodId": 1,
        "updatedAt": "string",
        "workCost": 1,
        "workCostDefault": 1,
        "workCostNormalized": 1
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
        "creator": {
          "meta": {
            "included": true
          }
        },
        "dealSubsidiary": {
          "meta": {
            "included": true
          }
        },
        "invoiceAttribution": {
          "meta": {
            "included": true
          }
        },
        "lastActor": {
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
        "person": {
          "meta": {
            "included": true
          }
        },
        "personSubsidiary": {
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
        "task": {
          "meta": {
            "included": true
          }
        },
        "timesheet": {
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
| `attributes.billableTime` | number |  |
| `attributes.calendarEventId` | string |  |
| `attributes.cost` | number |  |
| `attributes.costDefault` | number |  |
| `attributes.costNormalized` | number |  |
| `attributes.createdAt` | string |  |
| `attributes.currency` | string |  |
| `attributes.currencyDefault` | string |  |
| `attributes.currencyNormalized` | string |  |
| `attributes.date` | string |  |
| `attributes.facilityOverheadCost` | number |  |
| `attributes.facilityOverheadCostDefault` | number |  |
| `attributes.facilityOverheadCostNormalized` | number |  |
| `attributes.internalOverheadCost` | number |  |
| `attributes.internalOverheadCostDefault` | number |  |
| `attributes.internalOverheadCostNormalized` | number |  |
| `attributes.invoiceAttributionId` | string |  |
| `attributes.invoiced` | boolean |  |
| `attributes.lastActivityAt` | string |  |
| `attributes.note` | string |  |
| `attributes.overhead` | boolean |  |
| `attributes.overheadCost` | number |  |
| `attributes.overheadCostDefault` | number |  |
| `attributes.overheadCostNormalized` | number |  |
| `attributes.recognizedTime` | number |  |
| `attributes.rejected` | boolean |  |
| `attributes.rejectedAt` | string |  |
| `attributes.rejectedReason` | string |  |
| `attributes.startedAt` | string |  |
| `attributes.submitted` | boolean |  |
| `attributes.time` | number |  |
| `attributes.timerStartedAt` | string |  |
| `attributes.timerStoppedAt` | string |  |
| `attributes.trackMethodId` | number |  |
| `attributes.updatedAt` | string |  |
| `attributes.workCost` | number |  |
| `attributes.workCostDefault` | number |  |
| `attributes.workCostNormalized` | number |  |
| `id` | string |  |
| `relationships.approvalStatuses.meta.included` | boolean |  |
| `relationships.approver.meta.included` | boolean |  |
| `relationships.creator.meta.included` | boolean |  |
| `relationships.dealSubsidiary.meta.included` | boolean |  |
| `relationships.invoiceAttribution.meta.included` | boolean |  |
| `relationships.lastActor.meta.included` | boolean |  |
| `relationships.organization.data.id` | string |  |
| `relationships.organization.data.type` | string |  |
| `relationships.person.meta.included` | boolean |  |
| `relationships.personSubsidiary.meta.included` | boolean |  |
| `relationships.rejecter.meta.included` | boolean |  |
| `relationships.service.meta.included` | boolean |  |
| `relationships.task.meta.included` | boolean |  |
| `relationships.timesheet.meta.included` | boolean |  |
| `relationships.updater.meta.included` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Productive.io API, this operation is `GET /time_entries/{{id}}` (base URL `https://api.productive.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-entry.md) for the provider-specific parameters and requirements.

