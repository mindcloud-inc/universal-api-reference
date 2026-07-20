# Instasent: Get Project Attribute Specs



```
GET https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-project-attribute-specs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instasent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-project-attribute-specs?connectionId=$CONNECTION_ID&project=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-project-attribute-specs?${params}`, {
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
| `project` | string | yes | Instasent project uid. Use the uid value from List Projects, not the internal project id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entities": [
        {
          "adhocUid": {},
          "createdAt": "string",
          "createdByDatasourceType": {},
          "createdByDatasourceUid": {},
          "custom": true,
          "dataType": "string",
          "description": "string",
          "displayLabel": "string",
          "enabled": true,
          "eventBased": true,
          "important": true,
          "internal": true,
          "mappeable": true,
          "multivalue": 1,
          "readonly": true,
          "uid": "string",
          "unique": true,
          "updatedAt": "string",
          "visible": true,
          "visualType": "string"
        }
      ],
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
        ],
        "uniqueAttributes": [
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
| `entities[].adhocUid` | object |  |
| `entities[].createdAt` | string |  |
| `entities[].createdByDatasourceType` | object |  |
| `entities[].createdByDatasourceUid` | object |  |
| `entities[].custom` | boolean |  |
| `entities[].dataType` | string |  |
| `entities[].description` | string |  |
| `entities[].displayLabel` | string |  |
| `entities[].enabled` | boolean |  |
| `entities[].eventBased` | boolean |  |
| `entities[].important` | boolean |  |
| `entities[].internal` | boolean |  |
| `entities[].mappeable` | boolean |  |
| `entities[].multivalue` | number |  |
| `entities[].readonly` | boolean |  |
| `entities[].uid` | string |  |
| `entities[].unique` | boolean |  |
| `entities[].updatedAt` | string |  |
| `entities[].visible` | boolean |  |
| `entities[].visualType` | string |  |
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
| `metadata.uniqueAttributes[]` | string |  |

## Native endpoint

Through the native Instasent API, this operation is `GET /project/:project/specs/attributes` (base URL `https://api.instasent.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-attribute-specs.md) for the provider-specific parameters and requirements.

