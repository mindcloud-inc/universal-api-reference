# GoTeamup: List Customer Forms

Finds customer forms in GoTeamup.

```
GET https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-customer-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-customer-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-customer-forms?${params}`, {
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
      "count": 1,
      "next": {},
      "previous": {},
      "results": [
        {
          "createdAt": "string",
          "fields": "string",
          "forceStaleUpdates": true,
          "id": 1,
          "memberships": "string",
          "membershipsAppliesTo": "string",
          "name": "Ava Chen",
          "offeringTypes": "string",
          "offeringTypesAppliesTo": "string",
          "order": 1,
          "submissionsExpireAfter": {}
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `next` | object |  |
| `previous` | object |  |
| `results[].createdAt` | string |  |
| `results[].fields` | string |  |
| `results[].forceStaleUpdates` | boolean |  |
| `results[].id` | number |  |
| `results[].memberships` | string |  |
| `results[].membershipsAppliesTo` | string |  |
| `results[].name` | string |  |
| `results[].offeringTypes` | string |  |
| `results[].offeringTypesAppliesTo` | string |  |
| `results[].order` | number |  |
| `results[].submissionsExpireAfter` | object |  |

## Native endpoint

Through the native GoTeamup API, this operation is `GET /customer_forms` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-forms.md) for the provider-specific parameters and requirements.

