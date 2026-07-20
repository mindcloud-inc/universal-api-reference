# Instasent: List Projects



```
GET https://connect.mindcloud.co/v1/universal/instasent/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instasent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instasent/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instasent/latest/actions/list-projects?${params}`, {
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
      "entity": {
        "callbackUrl": {},
        "createdAt": "string",
        "id": "string",
        "projects": [
          {
            "attributionConfig": {},
            "brand": {},
            "businessContactsSize": {},
            "businessType": "string",
            "businessUrl": {},
            "conversionConfig": {},
            "createdAt": "string",
            "defaultSmsSender": {},
            "description": "string",
            "generalConfig": {},
            "id": "string",
            "locale": "string",
            "lockedReason": {},
            "lockedUntil": {},
            "name": "Ava Chen",
            "projectStatus": "string",
            "projectType": "string",
            "shortTrackingDomain": {},
            "timezone": "string",
            "uid": "string",
            "unsubscribeTrackingDomain": {},
            "updatedAt": "string"
          }
        ],
        "support": [
          "string"
        ],
        "testMode": true,
        "title": "string",
        "token": "string"
      },
      "metadata": {
        "organization": {
          "account": {
            "credit": {
              "currency": "string",
              "resetAt": {},
              "resetTo": 1,
              "value": 1
            },
            "funds": {
              "currency": "string",
              "value": 1
            }
          },
          "api": {
            "tier": 1
          },
          "id": "string",
          "name": "Ava Chen",
          "plan": {
            "key": "string",
            "quality": 1,
            "status": "string"
          }
        },
        "scopes": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity.callbackUrl` | object |  |
| `entity.createdAt` | string |  |
| `entity.id` | string |  |
| `entity.projects[].attributionConfig` | object |  |
| `entity.projects[].brand` | object |  |
| `entity.projects[].businessContactsSize` | object |  |
| `entity.projects[].businessType` | string |  |
| `entity.projects[].businessUrl` | object |  |
| `entity.projects[].conversionConfig` | object |  |
| `entity.projects[].createdAt` | string |  |
| `entity.projects[].defaultSmsSender` | object |  |
| `entity.projects[].description` | string |  |
| `entity.projects[].generalConfig` | object |  |
| `entity.projects[].id` | string |  |
| `entity.projects[].locale` | string |  |
| `entity.projects[].lockedReason` | object |  |
| `entity.projects[].lockedUntil` | object |  |
| `entity.projects[].name` | string |  |
| `entity.projects[].projectStatus` | string |  |
| `entity.projects[].projectType` | string |  |
| `entity.projects[].shortTrackingDomain` | object |  |
| `entity.projects[].timezone` | string |  |
| `entity.projects[].uid` | string |  |
| `entity.projects[].unsubscribeTrackingDomain` | object |  |
| `entity.projects[].updatedAt` | string |  |
| `entity.support[]` | string |  |
| `entity.testMode` | boolean |  |
| `entity.title` | string |  |
| `entity.token` | string |  |
| `metadata.organization.account.credit.currency` | string |  |
| `metadata.organization.account.credit.resetAt` | object |  |
| `metadata.organization.account.credit.resetTo` | number |  |
| `metadata.organization.account.credit.value` | number |  |
| `metadata.organization.account.funds.currency` | string |  |
| `metadata.organization.account.funds.value` | number |  |
| `metadata.organization.api.tier` | number |  |
| `metadata.organization.id` | string |  |
| `metadata.organization.name` | string |  |
| `metadata.organization.plan.key` | string |  |
| `metadata.organization.plan.quality` | number |  |
| `metadata.organization.plan.status` | string |  |
| `metadata.scopes[]` | string |  |

## Native endpoint

Through the native Instasent API, this operation is `GET /` (base URL `https://api.instasent.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

