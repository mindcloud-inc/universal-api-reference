# GrowthBook: Delete a rule from a draft revision

Deletes a rule from a GrowthBook feature revision.

```
DELETE https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/delete-feature-revision-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/delete-feature-revision-rule?connectionId=$CONNECTION_ID&id=prj_19g6smo332up7&version=1&ruleId=rule_1&environment=production" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "prj_19g6smo332up7",
  "version": "1",
  "ruleId": "rule_1",
  "environment": "production"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/delete-feature-revision-rule?${params}`, {
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
| `id` | string | yes | Default: `prj_19g6smo332up7`. |
| `version` | number | yes | Default: `1`. |
| `ruleId` | string | yes | Default: `rule_1`. |
| `environment` | string | yes | Default: `production`. |
| `revisionTitle` | string | no |  |
| `revisionComment` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "revision": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `revision` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `DELETE /features/:id/revisions/:version/rules/:ruleId` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-feature-revision-rule.md) for the provider-specific parameters and requirements.

