# CustomGPT.ai: List Sources

Retrieves sources from a CustomGPT.ai agent.

```
GET https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/list-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomGPT.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/list-sources?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/list-sources?${params}`, {
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
| `projectId` | number | yes | The project ID whose sources should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "confluences": [
        {}
      ],
      "googleDrives": [
        {}
      ],
      "notions": [
        {}
      ],
      "oneDrives": [
        {}
      ],
      "sharepoints": [
        {}
      ],
      "sharepointSites": [
        {}
      ],
      "sitemaps": [
        {}
      ],
      "uploads": [
        {}
      ],
      "youtubes": [
        {}
      ],
      "zapiers": [
        {}
      ],
      "zendesks": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confluences` | array<object> | Confluence-backed sources grouped by provider response bucket. |
| `googleDrives` | array<object> | Google Drive-backed sources grouped by provider response bucket. |
| `notions` | array<object> | Notion-backed sources grouped by provider response bucket. |
| `oneDrives` | array<object> | OneDrive-backed sources grouped by provider response bucket. |
| `sharepoints` | array<object> | SharePoint-backed sources grouped by provider response bucket. |
| `sharepointSites` | array<object> | SharePoint site sources grouped by provider response bucket. |
| `sitemaps` | array<object> | Sitemap-backed sources grouped by provider response bucket. |
| `uploads` | array<object> | Uploaded-file sources grouped by provider response bucket. |
| `youtubes` | array<object> | YouTube-backed sources grouped by provider response bucket. |
| `zapiers` | array<object> | Zapier-backed sources grouped by provider response bucket. |
| `zendesks` | array<object> | Zendesk-backed sources grouped by provider response bucket. |

## Native endpoint

Through the native CustomGPT.ai API, this operation is `GET /projects/:projectId/sources` (base URL `https://app.customgpt.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sources.md) for the provider-specific parameters and requirements.

