# GrowthBook: Submit list of code references

Submits code references to your GrowthBook organization.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-code-refs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-code-refs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "branch": "sample",
  "repoName": "sample",
  "refs[]": [
    "sample"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-code-refs', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "branch": "sample",
    "repoName": "sample",
    "refs[]": ["sample"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deleteMissing` | string | no | Whether to delete code references that are no longer present in the submitted data |
| `branch` | string | yes | Default: `sample`. |
| `repoName` | string | yes | Default: `sample`. |
| `refs[]` | array<object> | yes | Default: `["sample"]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "featuresUpdated": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `featuresUpdated` | array<string> |  |

## Native endpoint

Through the native GrowthBook API, this operation is `POST /code-refs` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-code-refs.md) for the provider-specific parameters and requirements.

