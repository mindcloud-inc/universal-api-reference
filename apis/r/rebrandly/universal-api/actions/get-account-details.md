# Rebrandly: Get Account Details

Retrieves details for the current Rebrandly account.

```
GET https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/get-account-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrandly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/get-account-details?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarUrl": "https://example.com",
      "clicks": 1,
      "createdAt": "string",
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "id": "string",
      "registration": {
        "country": "string"
      },
      "scans": {
        "qr": 1
      },
      "subscription": {
        "addonsEligible": true,
        "billing": {
          "cycle": {
            "price": {
              "full": 1,
              "net": 1,
              "vat": 1
            },
            "recurrence": {
              "unit": "string",
              "units": 1
            },
            "resetsAt": "string",
            "trial": {
              "expiresAt": {}
            }
          }
        },
        "category": "string",
        "categoryVariant": "string",
        "createdAt": "string",
        "due": 1,
        "external": {
          "id": {},
          "line": {}
        },
        "id": "string",
        "limits": {
          "apps": {
            "included": 1,
            "used": 1
          },
          "cycle": {
            "clicks": {
              "included": 1,
              "used": 1
            },
            "linksClassic": {
              "included": 1,
              "used": 1
            }
          },
          "domains": {
            "included": 1,
            "used": 1
          },
          "scripts": {
            "included": 1,
            "used": 1
          },
          "tags": {
            "included": 1,
            "used": 1
          },
          "webhooks": {
            "included": 1,
            "used": 1
          },
          "workspaces": {
            "included": 1,
            "used": 1
          }
        },
        "plan": {
          "id": "string",
          "isSlg": true
        },
        "status": {
          "renew": true,
          "suspend": true
        },
        "version": 1
      },
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string |  |
| `clicks` | number |  |
| `createdAt` | string |  |
| `email` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `registration.country` | string |  |
| `scans.qr` | number |  |
| `subscription.addonsEligible` | boolean |  |
| `subscription.billing.cycle.price.full` | number |  |
| `subscription.billing.cycle.price.net` | number |  |
| `subscription.billing.cycle.price.vat` | number |  |
| `subscription.billing.cycle.recurrence.unit` | string |  |
| `subscription.billing.cycle.recurrence.units` | number |  |
| `subscription.billing.cycle.resetsAt` | string |  |
| `subscription.billing.cycle.trial.expiresAt` | object |  |
| `subscription.category` | string |  |
| `subscription.categoryVariant` | string |  |
| `subscription.createdAt` | string |  |
| `subscription.due` | number |  |
| `subscription.external.id` | object |  |
| `subscription.external.line` | object |  |
| `subscription.id` | string |  |
| `subscription.limits.apps.included` | number |  |
| `subscription.limits.apps.used` | number |  |
| `subscription.limits.cycle.clicks.included` | number |  |
| `subscription.limits.cycle.clicks.used` | number |  |
| `subscription.limits.cycle.linksClassic.included` | number |  |
| `subscription.limits.cycle.linksClassic.used` | number |  |
| `subscription.limits.domains.included` | number |  |
| `subscription.limits.domains.used` | number |  |
| `subscription.limits.scripts.included` | number |  |
| `subscription.limits.scripts.used` | number |  |
| `subscription.limits.tags.included` | number |  |
| `subscription.limits.tags.used` | number |  |
| `subscription.limits.webhooks.included` | number |  |
| `subscription.limits.webhooks.used` | number |  |
| `subscription.limits.workspaces.included` | number |  |
| `subscription.limits.workspaces.used` | number |  |
| `subscription.plan.id` | string |  |
| `subscription.plan.isSlg` | boolean |  |
| `subscription.status.renew` | boolean |  |
| `subscription.status.suspend` | boolean |  |
| `subscription.version` | number |  |
| `username` | string |  |

## Native endpoint

Through the native Rebrandly API, this operation is `GET /account` (base URL `https://api.rebrandly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-details.md) for the provider-specific parameters and requirements.

