# GrowthBook: Create a visual changeset for an experiment

Creates a visual changeset for a GrowthBook experiment.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-visual-changesets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-visual-changesets" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "prj_19g6smo332up7",
  "editorUrl": "https://example.com",
  "urlPatterns[]": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-visual-changesets', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "prj_19g6smo332up7",
    "editorUrl": "https://example.com",
    "urlPatterns[]": "https://example.com",
    "urlPatterns[]": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The id of the requested resource Default: `prj_19g6smo332up7`. |
| `editorUrl` | string | yes | URL of the page opened in the visual editor when creating this changeset Default: `https://example.com`. |
| `urlPatterns[]` | array<object> | yes | URL patterns that determine which pages this visual changeset applies to Default: `https://example.com`. |
| `urlPatterns[]` | array<object> | yes | URL patterns that determine which pages this visual changeset applies to Default: `https://example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "visualChangeset": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `visualChangeset` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `POST /experiments/:id/visual-changesets` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-visual-changesets.md) for the provider-specific parameters and requirements.

